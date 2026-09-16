# GANGLION

Fleet execution layer. Work is written down as intent, a router decides who runs it, and a machine somewhere picks it up and does it.

## The problem

Anything that automates real work eventually needs to run commands on more than one machine. The usual answer is a queue with workers attached to it, which works until the machines stop being interchangeable - this one has the GPU, that one has the Windows-only device attached, the other one is the only box with unrestricted outbound network. At that point "give the job to any free worker" stops being correct, and most systems solve it by hardcoding which worker gets which job. That hardcoding is the thing that rots.

There is a second problem underneath it. Once an automated system can run shell commands on your machines, the interesting question is not whether it works but what stops it doing something it should not. A queue has no opinion about that. Anything that can write to the queue can, in effect, do anything.

## What it does

GANGLION separates **what needs doing** from **who does it**. A request is written as an intent row - a lane, a target, the capabilities it requires, and the work itself - and nothing more. No machine is named.

A router reads those rows and decides. It matches required capabilities against the effectors currently alive, applies a capacity check and a safety check, and only then assigns. Effectors advertise what they can do rather than what they are: one has full outbound network and Linux tooling, another has a Windows filesystem and locally attached devices, another is ephemeral cloud with no persistent disk. New capability, new effector, no routing table to edit.

**Authority is explicit and it is not carried by the text of the request.** Routine work - read a file, run a build, commit - is covered by preauthorised action classes. Anything more sensitive needs a signature computed from a secret the requester has to actually hold. A request cannot talk its way into a privileged action by asserting that it is allowed to; an unsigned request that claims authorisation is simply an unsigned request. This turns out to matter, because the natural failure mode of an instruction-following system is that a convincing instruction is indistinguishable from a legitimate one.

Routers run in more than one place and elect a leader through an advisory lock, so exactly one is promoting work at a time and the standby takes over without coordination. Effectors heartbeat; a silent one is considered stale and its claims are reaped and reissued.

## Part of a system

GANGLION is the execution layer for a larger cognitive-infrastructure stack. See [davidkirsch.me/builds](https://davidkirsch.me/builds) for the rest.
