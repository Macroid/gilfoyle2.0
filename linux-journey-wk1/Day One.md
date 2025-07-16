# edX Intro to Linux

Link: https://learning.edx.org/course/course-v1:LinuxFoundationX+LFS101x+1T2025/home
## The Linux Foundation

- Leading home for collabs on OSS and hardware
- Projects include Linux, Kubernetes, PyTorch, RISC-V, and many more
- Focus on best practices and needs of users
- Great meetups/events

## Course Software Requirements

Need a distro. Select:

- Red Hat Family
	- CentOS
	- CentOS Stream
	- Fedora
	- Oracle
- SUSE Family
	- SLES (SUSE Linux Enterprise Server)
	- openSUSE
- Debian Family
	- Ubuntu
	- Linux Mint

TLF is distribution-flexible. Efforts should work on almost all modern distros. Might need new packages. TLF focuses on GNOME as it is most widely used.

# Unix Philosophy

Link: https://en.wikipedia.org/wiki/Unix_philosophy

- Developed by Ken Thompson and Dennis Ritchie
- Build simple, compact, clear, modular, extensible code that is easily maintained

Captured by Doug Mcllroy:
1. Make each program do one thing well. To do a new job, build afresh rather than complicate old programs by adding new "features."
2. Expect the output of every program to become the input to another, as yet unknown, program. Don't clutter output with extraneous information. Avoid stringently columnar or binary input formats. Don't insist on interactive input.
3. Design and build software, even operating systems, to be tried early, ideally within weeks. Don't hesitate to throw away the clumsy parts and rebuild them.
4. Use tools in preference to unskilled help to lighten a programming task, even if you have to detour to build the tools and expect to throw some of them out after you've finished using them.

**Do One Thing and Do It Well**

# Mike Gancarz - Unix Tenets

1) Small is beautiful.
2) Make each program do one thing well.
3) Build a prototype as soon as possible.
4) Choose portability over efficiency.
5) Store data in flat text files.
6) User software leverage to your advantage.
7) Use shell scripts to increase leverage and portability.
8) Avoid captive user interfaces.
9) Make every program a filter.


# VMs for MacOS

- Parallels ($65)
- Virtual Box (free)
- (UTM $10 or free)

1) Purchased UTM through Apple Store
2) Found Ubuntu 23.04 for Apple Silicon (arm64)
3) Installed on UTM
4) **uname -a output** Linux Chris-VM 5.19.0-21-generic \#21-Ubuntu SMP PREEMPT_DYNAMIC Wed Oct 12 18:35:23 UTC 2022 aarch64 aarch64 aarch64 GNU/Linux
5) **lsb-release -a output:** 
> No LSB modules are available.
	Distributor ID:	Ubuntu
	Description:	Ubuntu Lunar Lobster (development branch)
	Release:	23.04
	Codename:	lunar
6) **man uname output:** 
```

UNAME(1)                         User Commands                        UNAME(1)

NAME
       uname - print system information

SYNOPSIS
       uname [OPTION]...

DESCRIPTION
       Print certain system information.  With no OPTION, same as -s.

       -a, --all
              print  all  information,  in the following order, except omit -p
              and -i if unknown:

       -s, --kernel-name
              print the kernel name

       -n, --nodename
              print the network node hostname

       -r, --kernel-release
              print the kernel release

```

# Missing Semester

## In the Shell

#linuxcommands

**date** - prints the time and date
**echo {arg}** - prints the argument. "echo $PATH" prints directories OS searches to find executable files.
**pwd** - prints working directory
