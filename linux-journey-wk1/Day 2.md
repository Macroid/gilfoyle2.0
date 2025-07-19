| Block               | Activity                                                                                                                                                                                                                                                       | Done |
| ------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---- |
| **1 h Read**        | Work through LinuxCommand.org “Learning the Shell – Lesson 2: Navigation.” ([linuxcommand.org](https://linuxcommand.org/lc3_lts0020.php?utm_source=chatgpt.com "Learning the shell - Lesson 2: Navigation - LinuxCommand.org"))                                | ✔    |
| **1 h Lab**         | In your VM create a nested directory tree (`~/play/alpha/beta`) and practice `pwd`, absolute vs relative `cd`, and listing variants (`ls -alh`, `ls -R`). Record outputs with `script` or copy-paste into notes.                                               | ✔    |
| **1 h Reference**   | Build a personal cheat-sheet for navigation commands, annotating options with **Devhints bash cheat-sheet** examples. ([linuxcommand.org](https://linuxcommand.org/?utm_source=chatgpt.com "LinuxCommand.org: Learn The Linux Command Line. Write Shell ...")) | ✔    |
| **1.5 h Challenge** | Start OverTheWire Bandit levels 0–3 (focus: login via SSH, reading files, moving between levels). ([overthewire.org](https://overthewire.org/wargames/bandit/?utm_source=chatgpt.com "Bandit - OverTheWire"))                                                  | ✔    |
| **0.5 h Commit**    | Push updated notes + `navigation_cheats.md` to the repo.                                                                                                                                                                                                       | ✔    |

# Lab

```
chris@Chris-VM:~$ cat ./typescript
Script started on 2025-07-17 23:57:51-04:00 [TERM="xterm-256color" TTY="/dev/pts/0" COLUMNS="80" LINES="24"]
chris@Chris-VM:~$ mkdir play
chris@Chris-VM:~$ cd play
chris@Chris-VM:~/play$ ls
chris@Chris-VM:~/play$ mkdir alpha
chris@Chris-VM:~/play$ cd alpha
chris@Chris-VM:~/play/alpha$ mkdir beta
chris@Chris-VM:~/play/alpha$ cd beta
chris@Chris-VM:~/play/alpha/beta$ pwd
/home/chris/play/alpha/beta
chris@Chris-VM:~/play/alpha/beta$ cd ..
chris@Chris-VM:~/play/alpha$ pwd
/home/chris/play/alpha
chris@Chris-VM:~/play/alpha$ cd ..
chris@Chris-VM:~/play$ pwd
/home/chris/play
chris@Chris-VM:~/play$ ls -R
.:
alpha

./alpha:
beta

./alpha/beta:
chris@Chris-VM:~/play$ ls -alh
total 12K
drwxrwxr-x  3 chris chris 4.0K Jul 17 23:58 .
drwxr-x--- 17 chris chris 4.0K Jul 17 23:57 ..
drwxrwxr-x  3 chris chris 4.0K Jul 17 23:58 alpha
chris@Chris-VM:~/play$ cd ..
chris@Chris-VM:~$ exit
exit

Script done on 2025-07-17 23:59:30-04:00 [COMMAND_EXIT_CODE="0"]
chris@Chris-VM:~$ 

```

