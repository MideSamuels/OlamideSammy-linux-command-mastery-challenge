# Day 23: Init Systems & systemctl Basics

Phase 5 - Process & Service Management | Day 23 of 30

Refer to [commands.md](./commands.md) for the 10 commands and systemctl operations practiced today, including their syntax and my own explanation of what each command does and when I would use it.

## What I practiced

I practiced managing Linux services with `systemctl`, including starting, stopping, restarting, and reloading services, configuring services to start automatically at boot, and checking their active and enabled states.

## What surprised me

What surprised me was learning that a service can be **active** without being **enabled**, because `systemctl is-active` checks its current running state while `systemctl is-enabled` checks whether it is configured to start automatically at boot.

## Evidence

The terminal output from my completed Day 23 systemctl practice is stored in [**evidence.md**](./evidence.md).

## Related

Previous day: [Day 22 - Controlling Processes with Signals](../day-22-process-signals/)

Next day: [Day 24 - Deeper Service Management & Logs](../day-24-service-logs/)

