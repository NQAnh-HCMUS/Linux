# Linux

## Linux Operating System and Applications: Linux Installation

### Chuẩn bị

Trước khi cài đặt cần chuẩn bị những phần sau:

- Chuột
- Đĩa cứng
- Màn hình
- Card mạng (nếu cài qua mạng)
- Chia partition đĩa cứng
- Mục tiêu cài đặt (cho server, cho workstation…)
- Phiên bản Linux (Fedora, Ubuntu, CentOS…)

### Phương thức cài đặt

- Linux có thể được cài đặt bởi nhiều nguồn:
  - Từ CD-ROM
  - Thông qua mạng (network)
- Có thể sử dụng chế độ đồ họa hay text để cài đặt

### Các bước cài đặt

- Thông thường, các phiên bản Linux sẽ cho lựa chọn cài đặt mới (install) hoặc nâng cấp (upgrade)
- Các bước thông thường gồm có:
  - Chọn install hoặc upgrade
  - Phân hoạch đĩa:
    - Có thể tạo ra các phân vùng (partition) mới hoặc dùng lại các partition Linux sẵn có
    - Chọn phân vùng swap
    - Chọn kiểu file system sử dụng
    - Format các phân vùng
- Tùy chọn các thông số software, hardware

### Phân vùng đĩa

- Phân vùng đĩa (`disk partitioning`) là công việc phân chia ổ đĩa cứng thành các vùng nhỏ khác nhau.
- Có ba loại phân vùng: `primary`, `extended` và `logical`
- Có thể có `tối đa 4 primary partitions` trên đĩa
- Các phân vùng `extended được tạo ra để chứa logical partitions`
- Phân vùng chứa `/boot phải nằm trong khoảng 1024 cylinder đầu tiên` đối với một số hệ máy cũ

### Swap space

- Swap space là một partition trên ổ cứng
- Linux sử dụng `swap space làm bộ nhớ ảo` (tương tự như pagefile trên windows)
- Cài đặt Linux `không có swap space sẽ làm giảm rõ rệt hiệu năng` của hệ thống
- `Có thể phân chia nhiều swap space` cho một hệ thống Linux
- Thông số được khuyên dùng: `swap = 2 * RAM`

### Các phân vùng cần thiết

- Phân vùng `/boot: Chứa thành phần khởi động hệ thống`
Linux
- Phân vùng `/swap`
- Phân vùng `/ (đọc là root): Chứa toàn bộ hệ điều hành` Linux

### Các loại file system

- Linux hỗ trợ khá nhiều định dạng file system khác nhau:
  - Ext2fs: được hỗ trợ từ phiên bản kernel 2.2 trở lên, không support journaling
  - Ext3fs: mạnh mẽ hơn phiên bản ext2, hỗ trợ journaling
  - XFS: được phát triển bởi SGI cho dòng vi xử lý 64 bit, hỗ trợ file có kích thước 8129 petabytes (1 triệu tỉ byte)
  - JFS: phát triển bởi IBM, hỗ trợ journaling

### Qui tắc đặt tên partition

- Các thiết bị trên Linux được đặt tên theo thứ tự:
  - IDE devices are named
    - /dev/hda, /dev/hdb, etc.
  - Logical partitions on /dev/hda
    - /dev/hdal, /dev/hda2, etc.
  - SCSI devices are named
    - /dev/sda, /dev/sdb, etc.
  - Logical partitions on /dev/sda
    - /dev/sdal, /dev/sda2, etc.

### Boot Loader

- Boot Loader là công cụ giúp `lựa chọn phiên bản hệ điều hành` nào được khởi động
- Linux hỗ trợ khá nhiều boot loader khác nhau:
  - LILO
  - GRUB
  - Choose-OS
  - System Commander
  - SYSLINUX
- Hai phiên bản thông dụng nhất là LILO và GRUB
  - Cài đặt từ đĩa CD-ROM
  - Cài đặt thông qua mạng
    - Sử dụng phần mềm Kickstart

### Giới thiệu một số tiện ích

- Open Office: Hỗ trợ các tính năng tương tự như bộ Microsoft Office. Với những phiên bản mới nhất, có thể đọc được file của MS Office 2007
- Libre Office: tương tự Open Office
- Web Browser
- Các giao diện Settings
- Các IDE lập trình
- Lập trình C++, Java
  - Eclipse
  - NetBeans
  - KDevelop

### History of Unix

- Origins at Bell Labs (1969–1971):
  - UNIX was created in 1969 at AT&T’s Bell Labs by Ken Thompson,
Dennis Ritchie, and others.
  - It started as a side project after the failure of the ambitious Multics
operating system.
  - Written in assembly at first, UNIX introduced a new philosophy:
simplicity, modularity, and reusability — with tools that do one thing
well.
- Portability Breakthrough (1973):
  - UNIX was rewritten in the C programming language, also developed at
Bell Labs.
  - This made UNIX highly portable, meaning it could be adapted to run on
different hardware — a revolutionary idea at the time.
History of Unix
- Early Expansion and Forks (1970s–1980s):
  - Version 6 UNIX (1975) became widely adopted in universities, especially
at UC Berkeley, where it evolved into BSD UNIX (Berkeley Software
Distribution).
  - AT&T continued developing its own versions (e.g., System III, System V).
  - Different organizations created their own variants, leading to the "UNIX
wars" of the 1980s.
- Commercialization and Standards (1980s–1990s):
  - UNIX became the basis for many commercial operating systems, such
as:
• SunOS/Solaris (Sun Microsystems)
• AIX (IBM)
• HP-UX (Hewlett-Packard)
  - Industry standards like POSIX and The Single UNIX Specification were
created to unify different versions.
History of Unix
- Influence on Linux and Modern Systems:
  - UNIX inspired Linux, which started in 1991 as a UNIX-like system using
GNU tools.
  - macOS, FreeBSD, and many embedded systems are UNIX or UNIX-like.
  - The UNIX philosophy shaped software engineering and operating system
design.
- UNIX Today:
  - While traditional commercial UNIX systems have declined, UNIX’s legacy
lives on through:
• Linux
• BSD variants (FreeBSD, OpenBSD)
• macOS (based on BSD UNIX)
  - The principles of UNIX — simplicity, composability, and transparency —
continue to influence modern computing.

1. Origins (Early 1990s):

- In 1991, Linus Torvalds, a Finnish computer science student, began developing a free, Unix-like operating system kernel as a personal project.
- He announced his work on a Usenet newsgroup, asking for feedback and contributions.
- The kernel was combined with GNU software (developed by the Free Software Foundation) to form a complete operating system: GNU/Linux.

2. Growth of Open Source Community:

- The project gained rapid support from developers worldwide due to its open-source license (GNU General Public License).
- Contributions came in the form of code, bug fixes, drivers, and utilities.

3. First Major Distributions (Mid 1990s):

- Distributions like Slackware (1993), Debian (1993), and Red Hat (1994) made Linux easier to install and use.
- These distros packaged the Linux kernel with system tools, GUIs, and software.

4. Adoption in Servers and Enterprises (2000s):

- Linux became popular for running web servers, databases, and enterprise applications due to its stability, performance, and cost-effectiveness.
- Companies like IBM and Oracle began supporting Linux.

5. Rise of Ubuntu and User-Friendliness (Mid 2000s):

- Ubuntu (2004) focused on ease of use, bringing Linux to desktops and making it accessible to a broader audience.

6. Cloud, Containers, and DevOps (2010s–Present):

- Linux became dominant in cloud computing, DevOps, and containerization (e.g., Docker, Kubernetes).
- Most cloud services (AWS, Google Cloud, Azure) use Linux as the base operating system.

7. Linux Today:

- Linux powers a wide range of systems: from supercomputers, web servers, and mobile devices (Android) to IoT devices and automotive systems.
- It is maintained by a global community, with support from companies like Red Hat (IBM), Canonical, Google, and others.

### Linux distro

- Derbian: Ubuntu, Knoppix, Raspbian/Raspberry Pi
- Red Hat (IBM): Fedora, Red Hat Enterprise Linux, CentOS
- openSUSE: SUSE Linux Enterprise
- Arch Linux
- Slackware
- Gentoo (Novel): Chrome OS

### Why Linux?

- Open Source and Free
  - No licensing fees — you can download, modify, and use it freely.
  - Full access to the source code gives developers control and transparency.
  - Encourages a global community of contributors and innovators.
- Stability and Reliability
  - Linux systems can run for years without rebooting.
  - It’s the top choice for servers, supercomputers, and critical infrastructure because of its uptime and fault tolerance.
- Security
  - Designed with multi-user architecture and permission controls.
  - Fewer vulnerabilities and faster security patches compared to many proprietary systems.
  - Preferred in cybersecurity and penetration testing fields.
- Performance and Efficiency
  - Low system requirements make it ideal for both modern hardware and older machines.
  - Frequently used in data centers, cloud platforms, and embedded devices for its performance-to-cost ratio.
- Flexibility and Customization
  - You can choose from hundreds of distributions, each tailored for a specific purpose (e.g., Ubuntu for desktops, CentOS for servers, Kali for security).
  - Highly configurable: you can build a minimal system or a full-featured desktop environment.
- Development-Friendly
  - Supports a wide range of programming languages and tools.
  - Ideal for software development, DevOps, and cloud-native application development.
  - Powers containers (Docker), orchestration tools (Kubernetes), and CI/CD pipelines.
- Community Support
  - Extensive documentation and forums.
  - Active user and developer communities provide troubleshooting help and updates.
- Ubiquity in Technology
  - Runs on everything: phones (Android), TVs, routers, cars, smart appliances, and more.
  - Dominates the cloud, web servers, and supercomputing industries.

### Companies that use Linux (Tech)

Company | How They Use Linux
---|---
Google | Runs on custom Linux servers and Android (a Linux-based OS)
Amazon | AWS uses Linux extensively (Amazon Linux, EC2, etc.)
Facebook (Meta) | Backend infrastructure is powered by Linux
Microsoft | Azure supports Linux VMs; contributes to the Linux kernel
IBM | Invested in Linux (owns Red Hat), uses Linux across enterprise solutions
Netflix | Uses Linux servers for streaming content globally
Twitter | Runs its entire infrastructure on Linux
Tesla | In-car systems and backend services use Linux
Intel | Develops and tests hardware with Linux support
Apple | While macOS is based on BSD Unix, Linux is widely used internally for testing and development

Company | Use Case
---|---
Goldman Sachs | Uses Linux for trading platforms and servers
JP Morgan | Chase Relies on Linux for secure, scalable systems
Deutsche Bank | Uses Linux in cloud-based financial services
CitiBank | Utilizes Linux for backend operations
Cisco | Networking hardware and routers run Linux
Verizon | Uses Linux in its telecom infrastructure
AT&T | Runs on Linux-based platforms in its networks

### What Can Linux Be Used For?

- Servers: Web, database, mail, and file servers
- Development: Programming, testing, and deployment
- Networking: System administration, firewalls, DNS, SSH
- Cybersecurity: Ethical hacking and security tools (e.g., Kali Linux)
- Cloud & DevOps: Containers, CI/CD, cloud infrastructure
- Embedded Systems: Routers, IoT devices, smart appliances
- Desktops: Personal computing, education, and multimedia

### Tools

- Linux: CentOS, Ubuntu
- VMware Workstation, Virtual Box
- Visual CertExam Manager
- Testking/ Pass4sure

## Linux Operating System and Applications: Command Line Basics

### Linux Directory Structure

Directory | Description
---|---
/boot | Kernel and boot configuration files
/bin | Essential user commands (binaries)
/dev | Device files (hardware interfaces)
/etc | System and application configuration files
/home | User home directories
/lib | Shared libraries required by binaries
/mnt | Mount point for temporary filesystems
/proc | Virtual filesystem for process and system info
/sbin | System administration commands
/tmp | Temporary files
/usr | User applications and libraries
/var | Variable data (e.g., logs, caches, spool files)

### File Naming Conventions in Linux

- `Maximum` length for a single file name is `255 characters` in most Linux file systems (like ext4).
- Linux `allows almost any character in file names`, including special characters such as ?, -, +, and spaces.
- File names can include letters, numbers, dots (.), underscores (_), and hyphens (-).
- File names are `case-sensitive` (File.txt ≠ file.txt).
- File names `can include extensions`, but they are not required or enforced by the system (e.g., .txt, .sh).
- File names `can contain spaces`, but it's better to avoid them. Use underscores (_) or hyphens (-) instead.
- `Hidden files (and directories) start with a dot “.”` Example: .bash_history

- Absolute Path
  - Starts with /
  - Full path from root
  - Examples: /, /bin, /usr, /usr/bin
- Relative Path
  - Does not start with /
  - Relative to current directory
  - Examples: etc/httpd/, usr/bin
- Special Notations
  - .. — Parent directory
  - . — Current directory
  - ~ — User’s home directory
  - Example: If current directory is /etc, the relative path to /etc/vsftp.conf is./vsftp.conf

### Kernel –

- The kernel is the core component of the Linux operating system. It manages and allocates system resources, including the CPU, memory (RAM), and hardware devices.
- Key Functions
  - Process scheduling – Controls which processes run and when
  - Memory management – Allocates and manages system memory
  - File system support – Provides access to files and directories
  - Process control – Creates and terminates processes
  - Device access – Manages communication with hardware devices
  - Network access – Handles data transmission over networks
  - System call interface – Provides APIs for applications to interact with the system

### SHELL

- The shell is a `command-line interpreter`, acting as a `special application` that `allows users to interact with the operating system`.
- Key Features
  - Interprets and executes commands
  - Provides simple scripting capabilities
  - Bridges user input and system-level operations
- Common Shells
  - sh – Bourne Shell
  - csh – C Shell
  - ksh – Korn Shell
  - bash – Bourne Again Shell (most widely used)

### Command Syntax

- General syntax: command [flags] arg1 arg2 …
  - Components are separated by spaces
  - Flags usually start with - (single-letter) or -- (multi-letter)
  - Examples
    - ls -a -l -F # Separate flags
    - ls --color # Long-format flag
    - ls -al # Combined short flags (same as -a -l)
- Notes
  - Some commands may not require a dash (-) before flags
  - Use --help or man to view help for a command:

      ls --help

      man ls
- To check which shell you're using: `echo $SHELL`

### Wildcard Characters in Linux

- File or directory names used as command-line arguments don’t always need to be explicit. You can use wildcards to match part or all of a name.
- Common wildcards
- Examples

Symbol | Meaning
---|---
$*$ | Matches any sequence of characters, including none
? | Matches any single character
[abc] | Matches one character from the set a, b, or c
[!abc] | Matches any character except a, b, or c
\ | Escapes special meaning of wildcards (e.g., \*, \?)

- Examples
  - ls *.txt → all files ending with .txt
  - ls file?.sh → matches file1.sh, fileA.sh, etc.
  - ls [a-c]* → files starting with a, b, or c

### Command Auto-Completion

Press the $<Tab>$ key to auto-complete commands, file names, or paths in the
terminal. If multiple matches exist, pressing $<Tab>$ twice shows suggestions.

$ cd /usr/lo<Tab>$ (/usr/local)

$ cp<Tab><Tab>$

cp cpp cpio cproto

$ cd dir<Tab><Tab>$

dir1 dir2 dir3

### Commonly Used Linux Commands

Command | Description
---|---
pwd | Show current working directory
cd | Change directory
ls | List directory contents
cp | Copy files and directories
mv | Move or rename files
rm | Remove files and directories
find | Search for files and directories
more | View file content one page at a time
grep | Print lines that match a given pattern
file | Determine the type of a file

### pwd and cd

- How to determine the current working directory?
  - Print working directory: pwd
- Change directory: cd
  - Examples:

$cd /etc$

$cd ~ ( ~: macro to indicate the user home directory)$

$cd /home/sv$

$cd ..$

$cd ../../data$

### echo

- Print a string to the screen
echo “Hello World”
- Print a string without a newline
echo –n “Enter your name:”

### ls

- Listing the directory contents

### mkdir, rmdir, touch

- mkdir – create a new directory
$ mkdir –p dir3/dir4
(flag -p: create the parent directory if it does not exists)
- rmdir – delete an empty directory
- touch – create a new empty file
$ touch file.txt

### cp, mv, rm, ln

- cp – copy file

$ cp file1 file2$

$ cp file1 dir1$

- -f : force overwrite without asking
- -i : prompt before overwriting
- -R,-r : copy the whole directory

$ cp –r dir1 dir2$

$cp -f source.txt destination.txt$

$cp -i source.txt destination.txt$

Output: overwrite 'destination.txt'? (y/n)

- mv – move/rename

$ mv file1 file2

$ mv dir1 dir2

- rm – delete file/directory

$ rm file1 file2

$ rm –r dir3

(flag -r: delete children files and directories)

- ln – is used to create links to files or directories (shortcut)

$ ln -s /path/to/dir1 firstdir

Create a symbolic (soft) link named firstdir that points to the directory dir1. After that, firstdir behaves like dir1.

$ ln –f /tmp/test.txt

Create a hard link to the file /tmp/test.txt in the current directory with the same name
(test.txt).

The -f option forces the link creation by removing any existing file with the same name.

### Wildcard Characters in cp, mv Commands

- $*$ matches any string, including the empty string

cp *.txt /backup/

- ? matches exactly one arbitrary character

mv file?.log /logs/

- […] matches any one of the characters inside the brackets

cp report[123].pdf /archive/

#copies report1.pdf, report2.pdf, or report3.pdf

- [!…] or [^…] matches any character not inside the brackets

mv data[!0-9].csv /data/

- \ removes the special meaning of the next character (escape character)

cp file?.txt /backup/

### Redirection

❑ Redirection: Redirecting Data Streams Elsewhere
❑ Types of Redirection:
❑ < : input redirection (read input from a file)
❑ > : output redirection (write output to a file, overwriting it)
❑ >> : output redirection (append output to the end of a file)
❑ Examples:
▪ ls -l / > /root/list.txt
Lists the contents of the / directory. The output is not shown on the screen, but
saved to the file /root/list.txt. If the file already exists, it will be overwritten.
▪ ls –l / >> /root/list.txt
Same as above, but instead of overwriting (>), the output will be appended to the
end of /root/list.txt.
Standard Data Streams
Example: Run the ls command, redirecting error messages to a file called error.txt:
ls -R / 2>/root/error.txt
This runs ls -R / (recursive listing of /) and sends all error messages (stderr) to
/root/error.txt.
Stream Number
stdin 0
stdout 1
stderr 2
Pipe
❑ Pipe: The output of one command is passed as the input to the next command,
using the | character
❑ Example: ls –R / | less
▪ The ls -R / command lists files recursively from /, and its output is sent to less
for paginated viewing.
❑ Paging with more and less:
▪ more lets you view output page by page.
▪ less provides more flexible navigation:
▪ Enter: to move down one line
▪ Spacebar: to move down one page
▪ b: to move back one page
▪ q: to quit
tee
❑ Output results both to the screen and to a file
❑ Example:
ls –l /etc | tee /root/list.txt

### String functions

❑ cat & tac
❑ head & tail
❑ nl & wc,
❑ od & hexdump
❑ join, sort, tr
❑ grep
cat & tac
❑ cat: View file contents
❑ Example: View the content of the file /etc/passwd
cat /etc/passwd
❑ Options:
▪ -n : number all output lines
▪ -b : number non-blank output lines only
▪ -A : display all characters, including line endings
❑ tac is the reverse of cat (displays file contents from the end
to the beginning)
head & tail
❑ head: View the first lines of data
❑ Examples:
▪ View the 4 first lines of the file /etc/passwd
head -4 /etc/passwd
cat /etc/passwd | head -4
▪ View the 4 first files or directories of the directory /
ls –l / | head -4
❑ tail: View the last lines of data
❑ Examples:
▪ View the 5 last lines of the file /etc/passwd
tail -5 /etc/passwd
cat /etc/passwd | tail -5
▪ View the contents of the file /etc/passwd starting from line 4 until the end:
tail –lines=+4 /etc/passwd
cat /etc/passwd | tail --lines=+4
❑ Note: The -f option allows tail to follow and continuously display appended data, useful for
monitoring dynamic log files.
wc: Lines, Words, Bytes count
❑ Syntax: wc [option] [files]
-l : count lines
-c or –m : count characters
-w : count words
❑ Examples:
▪ $ wc -l file1 - Counts the number of lines in file1
▪ $ wc file[123] - Counts lines, words, and bytes for the three
files file1, file2, and file3.
▪ $ wc -c file1 - Counts the number of characters (bytes) in
file1.
nl : Number Lines
❑ nl
❑ Example:
ls –l / | nl
View the list of files with line numbers.

#### join

❑ Syntax: join [
options]
file1 file2
▪ Options: -j field
❑ Example:
$ join file1 file2
$ join –j 1 file1 file2
File1: 1 one
2 two
3 three
File2: 1 11
2 22
4 44

#### tr – translate text

❑ Syntax: tr [options] [[string1 [string2]]
▪ Options: –d delete characters, -s : replace repeated characters with a single instance (squeeze)
$ cat file1 | tr a-z A-Z Convert lowercase letters to uppercase.
$ cat file1 | tr -d a Delete all occurrences of the character a
$ tr '[A-B]' '[a-b]'< file.txt Convert uppercase A and B to lowercase a and b
$ tr ':' ' ' < /etc/passwd Replace all characters : with spaces
$ cat file1 | tr -d abc Delete all occurrences of characters a, b, and c
[:lower:] lowercase letters
[:upper:] uppercase letters
[:alnum:] alphanumeric characters (letters and digits)
❑ Note: The tr command only accepts two arguments (string1 and string2).
cat file.txt | tr '[:lower:]' '[:upper:]'
cat file.txt | tr '[:upper:]' '[:lower:]'
cat file.txt | tr -d '[:alnum:]'
cat file.txt | tr -cd '[:alnum:]'
cut
❑ Syntax:
cut -d<delimiter> -f<field_number>
❑ Example: given a string
1;2;3;4;5;6
To extract the number 5 (the 5th field):
echo “1;2;3;4;5;6” | cut -d”;” -f5
Cutting Strings with awk
❑ Syntax: Print the n th field
awk -F<delimiter> '{ print $n }'
❑ By default, the delimiter is whitespace.
❑ Example: given the input string:
1;2;3;4;5;6
To extract the number 5 (the 5th field):
echo "1;2;3;4;5;6" | awk -F";" '{ print $5 }'

#### grep

❑ Searching Content with grep. Syntax:
grep [OPTION] PATTERN [FILE]
Options:
-i : case-insensitive search
-n : show line numbers with output
-r : recursively search in subdirectories
-v : invert match (show lines that do not match)
-w : match whole words only
❑ Examples:
grep root /etc/passwd : search for lines containing the word root in the file
/etc/passwd.
ls –l /etc/ | grep conf : find files containing the string conf in the /etc directory listing.


#### Regular Expressions for grep

❑ [abc] : matches character a, b, or c
❑ [a-h] : matches any one character from a to h
❑ [^abc] : matches any character except a, b, or c
❑ (ab|bc|cd) : matches ab or bc or cd
❑ ^ : matches the start of a line
❑ $ : matches the end of a line
❑ . : matches any single character
Number of occurrences:
- * : matches the preceding element 0 or more times
- + : matches the preceding element 1 or more times
find – file search command
find [path] [expression]
❑ $ find / -name “*.txt” : find file with the .txt extension in the
directory /
❑ $ find /usr/local -type f –print : find files only in /usr/local
❑ $ find /usr/X11R6 -type d : find directory only in /usr/X11R6
❑ $ find . -perm 755 -a -type f : find files with permission 755
in the current directory
Restart and Shutdown
❑ Shutdown:
init 0
or
shutdown –h now
❑ Restart:
init 6
or
shutdown –r now
init modes
❑ Syntax: init <number>
Runlevel Name Description
0 Shutdown Halts the system (power off). Safe to use when shutting down.
1 Single-user
mode
For maintenance. Only root can log in. No networking or multi-user support.
2 Multi-user (no
NFS)
Rarely used. Multi-user without network file system.
3 Multi-user mode Full multi-user with networking, but no graphical interface.
4 Undefined/Custo
m
Not used by default. You can customize it for special needs.
5 Graphical mode Multi-user mode with GUI login (X11/Display Manager).
6 Reboot Reboots the system.

#### history

The list of executed commands is stored in: “~/.bash_history”

- ^P, $<Up>$ previous command
- N, $<Down>$ next command
- history: display the list of previously executed commands

`$ history`

1 clear

2 cd /

3 ls

4 mkdir /tmp/dir1

- !n: re-execute command number n
- !string: re-execute the most recent command that starts with "string"

## Linux Operating System and Application: vi editor

### Introduction to the Vi Editor

What is Vi?

- Vi (pronounced “vee-eye”) is the default text editor in many UNIX systems.
- Introduced in 1976, it remains widely used today.
- A powerful and efficient command-line editor.
- Favored by system administrators for its speed and reliability.

Common Use Cases

- Editing configuration files.
- Writing scripts and notes.
- Editing source code.
- Creating simple text documents.

Vi vs. Vim

- Vi is the original editor; Vim ("Vi IMproved") is a more feature-rich version.
- On many systems, vi actually runs vim.

### Getting Started with Vi

Opening a File

- vi `<filename>` — Open or create a file.

Useful Options

- vi +n `<file>` — Start at line n.
- vi +/`<pattern>` `<file>` — Jump to first match of pattern.
- vi + `<file>` — Start at the last line.
- vi -r `<file>` — Recover a file after crash.

### Understanding Vi Modes

Two Main Modes

- Command Mode: Navigate and manipulate text (default on open).
- Insert Mode: Enter and modify text.

Switching Modes

- Command → Insert: i, a, o, A, O
- Insert → Command: Press Esc.

### Navigating in Command Mode

Character & Line Navigation

- h, j, k, l: Left, down, up, right.

Word & Line Navigation

- w, b, e: Next, previous, and end of word.
- 0, $: Start and end of line.

Screen Navigation

- G, gg, nG: Go to last, first, or line n.
- Ctrl-F/B: Forward/back one screen.
- Ctrl-D/U: Half screen scroll.

### Editing Text

- Insert Text
  - i, a, o, A, O: Enter Insert mode at various points.
- Delete Text
  - x, dd, dw, D: Delete character, line, word, to end of line.
- Change Text
  - r, R: Replace one or multiple characters.
  - cw, cc, cNw: Change word/line/N words.
- Undo
  - u: Undo last action (toggle behavior in Vi).

### Copying and Pasting

Copy (Yank)

- yy: Copy current line.
- Nyy: Copy N lines.
- yM: Copy a motion (e.g., y3w for 3 words).

Paste

- p: Paste after cursor.
- P: Paste before cursor.

### Saving and Quitting

Save

- :w — Save file.
- :w <filename> — Save as new file.

Quit

- :q — Quit (if no changes).
- :q! — Force quit without saving.

Save & Quit

- :wq or ZZ — Save and quit.

### Other Useful Commands

Searching

- /text — Search forward.
- ?text — Search backward.
- n, N — Next/previous match.

Line Numbers

- :set number / :set nonumber
- :.= — Show current line number.
- := — Show total line count.
- Ctrl-G — Show file and line info.

Joining Lines

- J: Join current line with next.

### Tips & Best Practices

- Case Sensitivity
  - Vi commands and searches are case-sensitive.
- Mouse Usage
  - Mouse does not move the cursor—use keyboard commands.
- Back Up Before Editing
  - Always copy critical files before using Vi.
- Practice Makes Perfect
  - Try commands on a sample file to build muscle memory.






















