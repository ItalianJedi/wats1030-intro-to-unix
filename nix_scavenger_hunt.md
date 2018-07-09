# *nix Scavenger Hunt

Complete the following challenges using the command-line interface on your favorite
Unix or Linux operating system. You are welcome and encouraged to consult any
additional documentation online or in books.

Please add your answers/responses/text pastes to the document after each prompt.

Note: For some of the challenges you will need to reference files included with
this repository, so you will need to fork the repo into your own Github account
and then clone it to your development environment.

## The Challenges

### Navigating the Filesystem

* Get an idea of where you are in the operating system. Use the `pwd` command to find your "path to working directory"--your current location in the filesystem of your devbox. *Paste the output of the `pwd` command here:* 
`user@869e0139263b:/projects$ pwd
/projects`

* Discover more about this filesystem. Use `ls` (the "list" command)to see what is in this directory. *What directories and files do you see when you run `ls`?*
user@869e0139263b:/projects$ ls
italianjedi.github.io   wats3010-adv-markup    wats3010-css             wats3010-hello-world           wats3010-product-page  wats3020-sandwich-machine
wats1030-intro-to-unix  wats3010-basic-markup  wats3010-embedded-media  wats3010-intro-to-bootstrap-4  wats3020-mad-libs


* You can use *options* to modify how a command runs. Try using `ls -alh` to see the contents of your current directory. *How are the results different when you use the `-alh` options?*
total 8.0K
drwxr-xr-x 12 user root  291 Jul  4 09:17 .
drwxr-xr-x 22 root root  295 Jul  4 09:13 ..
drwxr-xr-x  4 user root  100 Jun 28 18:45 italianjedi.github.io
drwxr-xr-x  5 user root  178 Jul  4 09:17 wats1030-intro-to-unix
drwxr-xr-x  4 user root  253 Apr 27 02:41 wats3010-adv-markup
drwxr-xr-x  4 user root  192 Apr 10 16:28 wats3010-basic-markup
drwxr-xr-x  5 user root  130 Apr 19 16:57 wats3010-css
drwxr-xr-x  7 user root  134 May  5 18:46 wats3010-embedded-media
drwxr-xr-x  4 user root   98 Apr  5 16:58 wats3010-hello-world
drwxr-xr-x 11 user root 4.0K May 18 18:41 wats3010-intro-to-bootstrap-4
drwxr-xr-x  6 user root 4.0K Jun 13 16:50 wats3010-product-page
drwxr-xr-x  6 user root  101 Jun 27 17:34 wats3020-mad-libs

//I think you may be asking what happens when we use -alh separately. Here is what I got then:
user@b69b56666bd5:/projects$ ls -a
.   italianjedi.github.io   wats3010-adv-markup    wats3010-css             wats3010-hello-world           wats3010-product-page  wats3020-sandwich-machine
..  wats1030-intro-to-unix  wats3010-basic-markup  wats3010-embedded-media  wats3010-intro-to-bootstrap-4  wats3020-mad-libs

user@b69b56666bd5:/projects$ ls -l
total 8
drwxr-xr-x  4 user root  100 Jun 28 18:45 italianjedi.github.io
drwxr-xr-x  5 user root  178 Jul  4 09:17 wats1030-intro-to-unix
drwxr-xr-x  4 user root  253 Apr 27 02:41 wats3010-adv-markup
drwxr-xr-x  4 user root  192 Apr 10 16:28 wats3010-basic-markup
drwxr-xr-x  5 user root  130 Apr 19 16:57 wats3010-css
drwxr-xr-x  7 user root  134 May  5 18:46 wats3010-embedded-media
drwxr-xr-x  4 user root   98 Apr  5 16:58 wats3010-hello-world
drwxr-xr-x 11 user root 4096 May 18 18:41 wats3010-intro-to-bootstrap-4
drwxr-xr-x  6 user root 4096 Jun 13 16:50 wats3010-product-page
drwxr-xr-x  6 user root  101 Jun 27 17:34 wats3020-mad-libs
drwxr-xr-x  7 user root  115 Jul  5 08:32 wats3020-sandwich-machine

user@b69b56666bd5:/projects$ ls -h
italianjedi.github.io   wats3010-adv-markup    wats3010-css             wats3010-hello-world           wats3010-product-page  wats3020-sandwich-machine
wats1030-intro-to-unix  wats3010-basic-markup  wats3010-embedded-media  wats3010-intro-to-bootstrap-4  wats3020-mad-libs

* The `man` ("manual") command tells you more about how any given command works. (*WARNING:* CodeAnywhere does not support the man command. You can click the following link to complete this task: http://man.he.net/). Run `man` to see instructions about how to use `man`. Then use `man` to learn what the `a`, `l`, and `h` options mean when used with the `ls` command. *Write down what those options do?*
I can't get this to work on Powershell or my command line so I found these by Googling it.
-a:Show all (including hidden)
-l:Long listing format
-h:Human-readable

They all look to display the same material but in different ways.

* Commands can also take *arguments*, which are usually the names of files or locations that you want the command to work with. Try running `ls /` to see what files are in the *root* directory of the filesystem. *What files and directories do you see listed?*
bin  boot  dev  etc  home  lib  lib64  media  mnt  open-jdk-source-file-location  opt  proc  projects  root  run  sbin  srv  sys  tmp  usr  var


* A Unix filesystem has a few special shortcuts to refer to specific locations. `/` indicates the *root* of the filesystem, meaning the top-most directory in the filesystem hierarchy. Use the `cd` ("change directory") command to move to the root directory. (Hint: Use `man` to look up the `cd` command if you have any issues) *Then run `pwd` and paste the output here:*
user@869e0139263b:/projects$ ls /
bin  boot  dev  etc  home  lib  lib64  media  mnt  open-jdk-source-file-location  opt  proc  projects  root  run  sbin  srv  sys  tmp  usr  var

* Another special shortcut in Unix is the `~` location. This indicates the *user root* directory, meaning the top-most directory in the hierarchy that comes below your user account. Use `cd` to move to `~`. *Run `pwd` and paste the response here:*
user@869e0139263b:/projects$ cd ~
user@869e0139263b:~$ pwd
/home/user


* Change directory into the `challenge_files` directory. Use `ls` to find only the files with a `.demo` pattern. *How many files do you find?*
user@869e0139263b:/projects$ cd wats1030-intro-to-unix/challenge_files/
user@f97ce9d74f7c:/projects/wats1030-intro-to-unix/challenge_files$ ls *.demo
2015_special_stuff.demo  cloaked-wookie.demo  scooter-double-mamba.demo


* Use the `cd` command to move "up" one directory. *Where are you in the filesystem now?*
user@f97ce9d74f7c:/projects/wats1030-intro-to-unix/challenge_files$ cd ..
/projects/wats1030-intro-to-unix

* Press the up arrow on your keyboard. *What just happened?*
pwd popped up which was my last command


* Press the up arrow a few more times. *What do you see?*
displayed the last couple commands

* Run the `history` command. *What do you see?*
It brought up the last couple commands I ran, which I ended up starting over half way through this project.
user@869e0139263b:/projects/wats1030-intro-to-unix/challenge_files$ history
    1  cd wats1030-intro-to-unix/challenge_files/
    2  ls *.demo
    3  cd up
    4  cd ..
    5  cd wats1030-intro-to-unix/challenge_files/
    6  pwd
    7  ls history
    8  history

### Observing the System

* Discover what account you are logged into using the `whoami` command. *What username are you currently using?*
user, this could be because I am doing this in codenvy

* Discover who else is on your system with the `who` command. *Are any other users using your system? If so, list them here:*
user@f97ce9d74f7c:/projects/wats1030-intro-to-unix$ who
user@f97ce9d74f7c:/projects/wats1030-intro-to-unix$
Looks like no one, again, probably because I am using codenvy

* How long has your system been running? Use `uptime` to see, and *paste the result here:*
user@f97ce9d74f7c:/projects/wats1030-intro-to-unix$ uptime
 06:42:39 up 2 days, 22:36,  0 users,  load average: 0.01, 0.03, 0.05

* Run `ps aux` and review the results. (Hint: Use `man` to learn more about the `ps` command and options.) *How do you interpret what you see here?*
It looks like active processes, according to man
user@f97ce9d74f7c:/projects/wats1030-intro-to-unix$ ps aux
USER       PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
user         1  0.0  0.0   4500   644 ?        Ss   05:18   0:00 /bin/sh -c tail -f /dev/null
root        18  0.0  0.0  47000  2004 ?        S    05:18   0:00 sudo /usr/sbin/sshd -D
user        19  0.0  0.0   6036   628 ?        S    05:18   0:00 tail -f /dev/null
root        20  0.0  0.0  65512  3276 ?        S    05:18   0:00 /usr/sbin/sshd -D
user       135  0.0  0.0   4508   748 ?        Ss   05:18   0:00 /bin/sh -c trap '[ -z "$(jobs -p)" ] || kill $(jobs -p); [ -e /tmp/docker-exec-186774.pid ] && rm /tmp/docker-exec-186774.pid
user       197  0.0  0.0  14792  6704 ?        Sl   05:18   0:00 /home/user/che/exec-agent/che-exec-agent -addr :4412 -cmd /bin/bash -path /[^/]+ -enable-auth -logs-dir /home/user/che/exec-a
user       219  0.0  0.0   4508   744 ?        Ss   05:18   0:00 /bin/sh -c trap '[ -z "$(jobs -p)" ] || kill $(jobs -p); [ -e /tmp/docker-exec-186777.pid ] && rm /tmp/docker-exec-186777.pid
user       273  0.0  0.0  16692  9852 ?        Sl   05:18   0:00 /home/user/che/terminal/che-websocket-terminal -addr :4411 -cmd /bin/bash -path /[^/]+ -enable-auth -enable-activity-tracking
user       286  0.0  0.0   4508   756 ?        Ss   05:18   0:00 /bin/sh -c trap '[ -z "$(jobs -p)" ] || kill $(jobs -p); [ -e /tmp/docker-exec-186780.pid ] && rm /tmp/docker-exec-186780.pid
user       346  1.0  1.4 5821740 445520 ?      Sl   05:18   0:56 /usr/lib/jvm/java-1.8.0-openjdk-amd64/bin/java -Djava.util.logging.config.file=/home/user/che/ws-agent/conf/logging.propertie
user       441  0.0  0.0  21084  3384 pts/0    Ss+  05:18   0:00 /bin/bash
user       496  0.0  0.0  21084  3388 pts/1    Ss+  05:22   0:00 /bin/bash
user       519  0.0  0.0  21084  3392 pts/2    Ss+  05:24   0:00 /bin/bash
user       842  0.0  0.0  21084  3392 pts/3    Ss+  06:25   0:00 /bin/bash
user       898  0.0  0.0  21084  3400 pts/4    Ss   06:31   0:00 /bin/bash
user       999  0.0  0.0  36076  1644 pts/4    R+   06:48   0:00 ps aux

* Run `top` and review the results. (Hint: You may need to use `ctrl-c` to get out of this app.) *How do you interpret what you see here?*
Real time view of the running system, according to man
top - 06:52:27 up 2 days, 22:46,  0 users,  load average: 0.01, 0.02, 0.05
Tasks:  16 total,   1 running,  15 sleeping,   0 stopped,   0 zombie
%Cpu(s):  0.0 us,  0.1 sy,  0.0 ni, 99.8 id,  0.0 wa,  0.0 hi,  0.0 si,  0.1 st
KiB Mem : 31231632 total, 21112012 free,  3220948 used,  6898672 buff/cache
KiB Swap: 12582908 total, 12580860 free,     2048 used. 27245892 avail Mem

  PID USER      PR  NI    VIRT    RES    SHR S  %CPU %MEM     TIME+ COMMAND
    1 user      20   0    4500    644    548 S   0.0  0.0   0:00.04 sh
   18 root      20   0   47000   2004   1580 S   0.0  0.0   0:00.00 sudo
   19 user      20   0    6036    628    536 S   0.0  0.0   0:00.00 tail
   20 root      20   0   65512   3276   2556 S   0.0  0.0   0:00.01 sshd
  135 user      20   0    4508    748    620 S   0.0  0.0   0:00.03 sh
  197 user      20   0   14792   6704   3236 S   0.0  0.0   0:00.22 che-exec-agent
  219 user      20   0    4508    744    620 S   0.0  0.0   0:00.03 sh
  273 user      20   0   17748  10328   3576 S   0.0  0.0   0:00.89 che-websocket-t
  286 user      20   0    4508    756    620 S   0.0  0.0   0:00.02 sh

### Finding and Viewing Files

* Make sure you are in the `challenge_files` directory. Use the `*` wildcard to find all the files that have the word "credit" in the filename. *How many files did you find?*
2
user@f97ce9d74f7c:/projects/wats1030-intro-to-unix/challenge_files$ ls *credit*
credit_cards2.txt  credit_cards.txt


* Use the `more` command to view one of the `credit_cards` files you just discovered. (Hint: Type `q` to quit viewing the file. Press the `spacebar` to page down. Use your keyboard arrows to move up/down.) *What is the date in the file you have viewed?*
user@f97ce9d74f7c:/projects/wats1030-intro-to-unix/challenge_files$ more credit_cards.txt
Last updated: 01-15-2015


* Use the `find` command to search for files more effectively. Search the sub-directories under `challenge_files` to find the location of the file named `modi_laboriosam.txt`. *Where is that file located?*
user@869e0139263b:/projects/wats1030-intro-to-unix/challenge_files$ find -name modi_laboriosam.txt
./tmp/modi_laboriosam.txt

* Use the `grep` command to search for text within a file. Use `grep` on all the `.user` files in `challenge_files` to find which files contain "WA" (the abbreviation for Washington state). *How many files did you find?*
user@0e0d300301f0:/projects/wats1030-intro-to-unix/challenge_files$ grep "WA" *.user
Britt-Erdman.user:O'Harachester, WA 37261
Lissie-Strosin.user:Jewessfurt, WA 00816-7241

* Use the `-r` option of `grep` to *recursively* find the text "Waldo" hidden in a file somewhere under the `challenge_files` directory. *Paste the result showing the file and line where the word "Waldo" shows up.*
user@0e0d300301f0:/projects/wats1030-intro-to-unix/challenge_files$ grep -r "Waldo"
serial-numbers/eaque_molestiae.txt:Ut est maiores quia autem. Nisi modi Waldo sed corporis sit explicabo ut est. Et est placeat ea sunt sunt consectetur sunt incidunt. Explicabo vel esse bla
nditiis dolorem culpa non quia.

### Pipes and Connecting Commands

* Sometimes it's useful to output the results of a command to a text file for further analysis, reference, or processing. Try running `ls > files.txt`. Notice that the file `files.txt` was created. View that file using `more`. *What do you see in the `files.txt` file?*
A list of files from the challenge_files folder

* Notice that if you run `ls -alh` in the `challenge_files` directory, the files scroll by very quickly. Sometimes it would be better to get the results in a paginated format. Try running `ls -alh | more`. *Describe what you see when you run `ls -alh | more`.*
when you put more at the end it stops after a few and when you hit return you get the next one, as opposed to just ls -alh which seems to give you the full list


* Earlier, when you viewed the list of active processes on your devbox using `ps aux`, the list was probably really long. You can make this list more manageable by using the pipe (`|`) to filter the results of `ps` using `grep`. Run `ps aux | grep <your_username>` to see what processes are running for your specific user. *Paste the list of processes that reference your username here:*
Because I am using codenvy and it showed my username being user, i got a long list of things that brought up user. Here are the first three lines:
user         1  0.0  0.0   4500   640 ?        Ss   17:56   0:00 /bin/sh -c tail -f /dev/null
user        14  0.0  0.0   6036   624 ?        S    17:57   0:00 tail -f /dev/null
user        31  0.0  0.0   4508   748 ?        Ss   17:57   0:00 /bin/sh -c trap '[ -z "$(jobs -p)" ] || kill $(jobs -p); [ -e /tmp/docker-exec-212151.pid ] && rm /tmp/docker-exec-212151.pi
