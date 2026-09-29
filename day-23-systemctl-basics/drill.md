# Day 23 Drill: Init Systems & systemctl Basics

## Objective

Pick a service, stop it, confirm it is inactive, restart it, enable it to auto-start at boot in a single combined command, and confirm both its active and enabled state.

## Steps Completed

1. Selected a service available on the Ubuntu system.
2. Stopped the service using `systemctl stop`.
3. Confirmed that the service was inactive using `systemctl is-active`.
4. Restarted the service using `systemctl restart`.
5. Enabled and started the service using `systemctl enable --now`.
6. Confirmed that the service was active using `systemctl is-active`.
7. Confirmed that the service was enabled using `systemctl is-enabled`.
8. Recorded the relevant terminal output as evidence.

## Commands Actually Run

```bash
systemctl stop <service-name>

systemctl is-active <service-name>

systemctl restart <service-name>

systemctl enable --now <service-name>

systemctl is-active <service-name>

systemctl is-enabled <service-name>
```

## Results

The selected service was successfully stopped and confirmed as inactive.

I restarted the service and then used `systemctl enable --now` to enable it to start automatically at boot while also starting it immediately.

The final checks confirmed that the service was active and enabled.

## Problems Encountered

One challenge was understanding the difference between a service being **active** and being **enabled**.

I learned that `systemctl is-active` checks whether a service is currently running, while `systemctl is-enabled` checks whether it is configured to start automatically at boot.

## Evidence

Terminal output from the completed Day 23 Init Systems & systemctl Basics drill is stored in `evidence.md` (./evidence.md).
