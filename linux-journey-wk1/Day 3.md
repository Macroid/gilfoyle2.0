| Block             | Activity                                                                                                                                                                                                                                                                                                                    | Done |
| ----------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---- |
| **1 h Read**      | Follow DigitalOcean’s “Basic Linux Navigation and File Management” tutorial sections on file viewing and management. ([DigitalOcean](https://www.digitalocean.com/community/tutorials/basic-linux-navigation-and-file-management?utm_source=chatgpt.com "Linux Navigation and File Management \| DigitalOcean"))            | ✅    |
| **1 h Lab**       | Download `/var/log/syslog` (or any sizeable text file) and experiment with `less N`, searching (`/error`), jumping (`G`, `g`), and piping `head`, `tail`. Capture five useful patterns in notes.                                                                                                                            | ✅    |
| **1 h Concept**   | Review “everything is a file” example: use `echo hello > /tmp/demo` then `cat /tmp/demo`; modify in place with `tee -a`. Document why redirection fits Unix philosophy. ([Wikipedia](https://en.wikipedia.org/wiki/Unix_philosophy?utm_source=chatgpt.com "Unix philosophy - Wikipedia"))                                   | ✅    |
| **1 h Reference** | Use **explainshell** to break down one complex command you met today; screenshot and save explanation. ([Reddit](https://www.reddit.com/r/commandline/comments/l5c0jg/explainshell_a_tool_that_takes_any_shell_commands/?utm_source=chatgpt.com "Explainshell - A tool that takes any shell commands, looks ... - Reddit")) | ✅    |
| **1 h Artifact**  | Commit `file_ops_examples.sh` and accompanying `readme`. (this doc)                                                                                                                                                                                                                                                         | ✅    |
# DigitalOcean

Added notes to navigation_cheats.md.

# Lab

## Head/tail

```
chris@Chris-VM:/var/log$ cat syslog | tail -n5
2025-07-18T22:50:11.951633-04:00 Chris-VM dbus-daemon[1071]: [session uid=1000 pid=1071] Successfully activated service 'org.gnome.DiskUtility'
2025-07-18T22:50:12.038679-04:00 Chris-VM dbus-daemon[1071]: [session uid=1000 pid=1071] Successfully activated service 'org.gnome.ArchiveManager1'
2025-07-18T22:50:12.101584-04:00 Chris-VM gnome-shell[1325]: DING: Detected async api for thumbnails
2025-07-18T22:50:12.157806-04:00 Chris-VM gnome-shell[1325]: DING: GNOME nautilus 43.1
2025-07-18T22:50:37.353447-04:00 Chris-VM systemd[1]: fprintd.service: Deactivated successfully.
chris@Chris-VM:/var/log$ cat syslog | head -n5
2025-07-15T22:20:21.235580-04:00 Chris-VM systemd[1]: Starting Flush Journal to Persistent Storage...
2025-07-15T22:20:21.235608-04:00 Chris-VM systemd[1]: Finished Apply Kernel Variables.
2025-07-15T22:20:21.235613-04:00 Chris-VM systemd[1]: Finished Load/Save Random Seed.
2025-07-15T22:20:21.235615-04:00 Chris-VM systemd[1]: First Boot Complete was skipped because of a failed condition check (ConditionFirstBoot=yes).
2025-07-15T22:20:21.235617-04:00 Chris-VM systemd-sysusers[314]: Creating group 'gamemode' with GID 999.
```

## less/search "error"
```
424 2025-07-15T22:20:21.236410-04:00 Chris-VM systemd[1]: Process error reports when automatic reporting is enabled
```

## g/G

- jumps to beginning (*g*) or end (*G*) of file when using *less*.

# Concept

```
chris@Chris-VM:/var/log$ echo hello > /tmp/demo
chris@Chris-VM:/var/log$ cat /tmp/demo
hello
chris@Chris-VM:/var/log$ tee -a /tmp/demo
very cool thing here
very cool thing here
^Z
[2]+  Stopped                 tee -a /tmp/demo
chris@Chris-VM:/var/log$ cat /tmp/demo
hello
very cool thing here
```

Very cool: tee -a lets you append real-time.

## Redirection
Redirection (">" or "<") is a fantastic fit to the Unix philosophy. Since Unix treats everything as a file, naturally, pushing data from file to program, and program to file is a hard requirement. Redirects facilitate that exactly.

# Explainshell demo

https://www.explainshell.com/explain?cmd=cat+syslog+%7C+head+-n5

