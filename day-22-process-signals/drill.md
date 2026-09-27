# Day 22 Drill: Controlling Processes with Signals

## Objective

Start a long-running command in the background, suspend it, resume it in the background, then start a second one that survives you logging out, using `nohup`.

## Steps Completed

1. Started a long-running command in the background.
2. Suspended the running process using `Ctrl+Z`.
3. Resumed the suspended process in the background using `bg`.
4. Brought the background process to the foreground using `fg`.
5. Started a second long-running command using `nohup`.
6. Confirmed that the second command was running independently of the terminal session.
7. Recorded the relevant terminal output as evidence.

## Commands Actually Run

```bash
sleep 300 &
```

```text
Ctrl+Z
```

```bash
bg
```

```bash
fg
```

```bash
nohup sleep 300 &
```

```bash
disown
```

## Results

The first long-running command was started in the background and assigned a job number by the shell.

I used `Ctrl+Z` to suspend the process and then used `bg` to resume it in the background.

I used `fg` to bring the background job back to the foreground.

I then started a second long-running command using `nohup` so that it could continue running independently of the terminal session.

Finally, I used `disown` to remove the background job from the shell's job table.

## Problems Encountered

One challenge was understanding the difference between suspending a foreground process, resuming it in the background, and bringing it back to the foreground.

I also learned that `nohup` is useful when a command needs to continue running after the terminal session ends.

## Evidence

Terminal output from the completed Day 22 Controlling Processes with Signals drill is stored in [evidence.md](./evidence.md).
