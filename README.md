# RHCSA8
#### Solution for RHCSA8 course tasks 
## About the Course
Red Hat Certified System Administrator (RHCSA) 3rd Edition  
Author: Sander Van Vugt  
The Red Hat Certified System Administrator (RHCSA), 3rd edition is all new and fully updated for RHEL 8. This course is designed to teach you everything you need to know to pass the RHCSA exam. Every objective in the exam is discussed, along with in-depth lessons on complex topics, so they are not confusing. Each lesson ends with a lab, so you can dive into your own projects and see Red Hat in action; many of these labs mimic scenarios you might find on the exam, so you get the experience you need to practice for the exam. These labs also include video solutions, so you can also see in real-time how to work through the problems and figure out the best methods for working through each scenario.  
<!-- #### [Download 50GB](https://rutracker.org/forum/viewtopic.php?t=5760295)
#### [Download 2.6GB](https://1337x.to/torrent/4315827/RHCSA-8-Red-Hat-Certified-System-Administrator-3rd-Edition-by-Sander-van-Vugt/) -->
## Index
- [lesson 2](#lesson2): Getting Started with Linux Commands
- [lesson 3](#lesson3): Essential File Management Tasks 
## <a name="lesson2"> Lesson 2
Getting Started with Linux Commands  
![lesson 2 task](./lesson2.png)
1.  - `mandb` update manual db
    - `man -k password` search for pages that contains word password
    - `man -k password | wc` count the results
    - unfortunatly we couldn't find any usefull results
2.  - `man useradd` and look for command in see also section
    - now we found `passwd` command
3.  - `useradd anna` add anna user first
    - `passwd anna` set a passwd for her
4.  - `cd /etc`
5.  - `ls -d *[0-9]*` note `-d` to list directories themselves, not their contents
6.  - `ls -l | less` then you can press `h` to browse commands 
7.  * some usefull commands in vim
    - `Esc` back to command mode
    - `i` insert mode
    - `a` append 
    - `o` open a new line
    - `:wq` write and quite
    - `:q!` quite and don't complain
    - `dd` delete a line
    - `yy` copy the current line
    - `p` past
    - `G`  goto the last line in the file
    - `gg` goto the beggining of the file
    - `d$` delete after cursor in line
    - `$` move cursor to the end of the line
    - `^` move cursor to the start of the line
    - `v` visual mode to select text
    - `u` undo
    - `Ctrl + r` redo
    - `/text` search for text forword
    - `?text` search for text backword
    - `:%s/old/new` for replacing text
## <a name="lesson3"> Lesson 3
Essential File Management Tasks 
![lesson 3 task](./lesson3.png)
1.  - `mkdir -p /tmp/files/pictures`
    - `mkdir -p /tmp/files/photos`
    - `mkdir -p /tmp/files/videos`
2.  - `cp /etc/[a-c]* /tmp/files/`
3.  - `mv /tmp/files/[a-b]* /tmp/files/photos/`
    - `mv /tmp/files/c* /tmp/files/videos/`
4.  - `find /etc/ -size -1000c -exec cp {} /tmp/files/pictures`
5.  - `ln -s /var/ /tmp/files/varlink`
6.  - `tar -cvJf /tmp/files/home.tar.xz /home`
    - `-J` for .xz compressing
7.  - `mkdir /tmp/arch/ ; tar -xvf /tmp/files/home.tar.xz -C /tmp/arch/`
    - note that we can use `Ctrl + a` to goto the start of the command line, and we can seperate commands using `;`