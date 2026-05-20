# Schedule Example

Recommended schedule:

```text
Daily at 08:00 local time.
```

RRULE:

```text
FREQ=DAILY;BYHOUR=8;BYMINUTE=0;BYSECOND=0
```

## Runtime Notes

Use a heartbeat automation when the goal is a thread digest that can run even when the local machine may be asleep.

Use a local cron only when the automation must write files directly to the local work-log vault. For local cron, schedule it when the machine is normally awake and do not assume missed runs will catch up automatically.
