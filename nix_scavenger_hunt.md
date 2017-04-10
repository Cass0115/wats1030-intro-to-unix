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
/Users/cassiedurr/Documents/wats1030-intro-to-unix

* Discover more about this filesystem. Use `ls` (the "list" command)to see what is in this directory. *What directories and files do you see when you run `ls`?*
LICENSE				nix_scavenger_hunt.md
README.md			nix_scavenger_hunt_stretch.md
challenge_files			super_scavengers.md

* You can use *options* to modify how a command runs. Try using `ls -alh` to see the contents of your current directory. *How are the results different when you use the `-alh` options?*
drwxr-xr-x@   9 cassiedurr  staff   306B Apr  6 16:13 .
drwx------+   6 cassiedurr  staff   204B Apr  6 17:35 ..
drwxr-xr-x   13 cassiedurr  staff   442B Apr  6 16:13 .git
-rw-r--r--    1 cassiedurr  staff   1.1K Apr  6 16:13 LICENSE
-rw-r--r--    1 cassiedurr  staff   2.7K Apr  6 16:13 README.md
drwxr-xr-x  111 cassiedurr  staff   3.7K Apr  6 16:13 challenge_files
-rw-r--r--    1 cassiedurr  staff   5.4K Apr  6 16:13 nix_scavenger_hunt.md
-rw-r--r--    1 cassiedurr  staff   317B Apr  6 16:13 nix_scavenger_hunt_stretch.md
-rw-r--r--    1 cassiedurr  staff   191B Apr  6 16:13 super_scavengers.md  

* The `man` ("manual") command tells you more about how any given command works. (*WARNING:* CodeAnywhere does not support the man command. You can click the following link to complete this task: http://linux.die.net/man/). Run `man` to see instructions about how to use `man`. Then use `man` to learn what the `a`, `l`, and `h` options mean when used with the `ls` command. *Write down what those options do?*


* Commands can also take *arguments*, which are usually the names of files or locations that you want the command to work with. Try running `ls /` to see what files are in the *root* directory of the filesystem. *What files and directories do you see listed?*
Applications			etc
Code				home
Library				installer.failurerequests
Network				net
System				private
Users				sbin
Volumes				tmp
bin				usr
cores				var
dev

* A Unix filesystem has a few special shortcuts to refer to specific locations. `/` indicates the *root* of the filesystem, meaning the top-most directory in the filesystem hierarchy. Use the `cd` ("change directory") command to move to the root directory. (Hint: Use `man` to look up the `cd` command if you have any issues) *Then run `pwd` and paste the output here:*
/Users/cassiedurr

* Another special shortcut in Unix is the `~` location. This indicates the *user root* directory, meaning the top-most directory in the hierarchy that comes below your user account. Use `cd` to move to `~`. *Run `pwd` and paste the response here:*
/Users/cassiedurr

* Change directory into the `challenge_files` directory. Use `ls` to find only the files with a `.demo` pattern. *How many files do you find?*
3

* Use the `cd` command to move "up" one directory. *Where are you in the filesystem now?*
wats1030-intro-to-unix

* Press the up arrow on your keyboard. *What just happened?*
It brings up the last command I typed

* Press the up arrow a few more times. *What do you see?*
Continues going up the commands

* Run the `history` command. *What do you see?*
A history of all the commands that I have ran.

### Observing the System

* Discover what account you are logged into using the `whoami` command. *What username are you currently using?*
cassiedurr

* Discover who else is on your system with the `who` command. *Are any other users using your system? If so, list them here:*
cassiedurr console  Mar 31 14:11
cassiedurr ttys000  Apr  6 17:35
Are those 2 different users?

* How long has your system been running? Use `uptime` to see, and *paste the result here:*
18:03  up 6 days,  3:52, 2 users, load averages: 2.04 1.63 1.43

* Run `ps aux` and review the results. (Hint: Use `man` to learn more about the `ps` command and options.) *How do you interpret what you see here?*
There is so much information that it is really hard to interpret. But it looks like they are programs that run on th computer at any given time. 

* Run `top` and review the results. (Hint: You may need to use `ctrl-c` to get out of this app.) *How do you interpret what you see here?*
It looks like it tells what is running on your computer, and what is sleeping. Also, how much memory it is taking

### Finding and Viewing Files

* Make sure you are in the `challenge_files` directory. Use the `*` wildcard to find all the files that have the word "credit" in the filename. *How many files did you find?*
2

* Use the `more` command to view one of the `credit_cards` files you just discovered. (Hint: Type `q` to quit viewing the file. Press the `spacebar` to page down. Use your keyboard arrows to move up/down.) *What is the date in the file you have viewed?*
1/15/15

* Use the `find` command to search for files more effectively. Search the sub-directories under `challenge_files` to find the location of the file named `modi_laboriosam.txt`. *Where is that file located?*
in the tmp sub folder.

* Use the `grep` command to search for text within a file. Use `grep` on all the `.user` files in `challenge_files` to find which files contain "WA" (the abbreviation for Washington state). *How many files did you find?*
Lissie-Strosin.user:Jewessfurt, WA 00816-7241                                                                                                           
Britt-Erdman.user:O'Harachester, WA 37261

* Use the `-r` option of `grep` to *recursively* find the text "Waldo" hidden in a file somewhere under the `challenge_files` directory. *Paste the result showing the file and line where the word "Waldo" shows up.*
serial-numbers/eaque_molestiae.txt:Ut est maiores quia autem. Nisi modi Waldo sed corporis sit explicabo ut est. Et est placeat ea sunt sunt consectetur
 sunt incidunt. Explicabo vel esse blanditiis dolorem culpa non quia.

### Pipes and Connecting Commands

* Sometimes it's useful to output the results of a command to a text file for further analysis, reference, or processing. Try running `ls > files.txt`. Notice that the file `files.txt` was created. View that file using `more`. *What do you see in the `files.txt` file?*


* Notice that if you run `ls -alh` in the `challenge_files` directory, the files scroll by very quickly. Sometimes it would be better to get the results in a paginated format. Try running `ls -alh | more`. *Describe what you see when you run `ls -alh | more`.*
total 460K                                                                                                                                              
drwxrwxr-x 7 cabox cabox 4.0K Apr 10 02:06 .                                                                                                            
drwxrwxr-x 4 cabox cabox 4.0K Apr  6 19:20 ..                                                                                                           
drwxrwxr-x 2 cabox cabox 4.0K Apr  6 19:20 01                                                                                                           
-rw-rw-r-- 1 cabox cabox    0 Apr  6 19:20 2015_special_stuff.demo                                                                                      
-rw-rw-r-- 1 cabox cabox   93 Apr  6 19:20 Afton-Jast.user                                                                                              
-rw-rw-r-- 1 cabox cabox   85 Apr  6 19:20 Aimee-Maggio.user                                                                                            
-rw-rw-r-- 1 cabox cabox   79 Apr  6 19:20 Alfonso-Gottlieb.user                                                                                        
-rw-rw-r-- 1 cabox cabox  100 Apr  6 19:20 Allen-Kemmer.user                                                                                            
-rw-rw-r-- 1 cabox cabox   86 Apr  6 19:20 Almina-Cormier.user                                                                                          
-rw-rw-r-- 1 cabox cabox   87 Apr  6 19:20 Alta-Lemke.user                                                                                              
-rw-rw-r-- 1 cabox cabox   79 Apr  6 19:20 Amina-McGlynn.user                                                                                           
-rw-rw-r-- 1 cabox cabox   78 Apr  6 19:20 Anabel-Hammes.user                                                                                           
-rw-rw-r-- 1 cabox cabox   61 Apr  6 19:20 Ancel-Conn.user                                                                                              
-rw-rw-r-- 1 cabox cabox   87 Apr  6 19:20 Anjali-Halvorson.user                                                                                        
-rw-rw-r-- 1 cabox cabox   64 Apr  6 19:20 Ardath-Kuvalis.user                                                                                          
-rw-rw-r-- 1 cabox cabox   90 Apr  6 19:20 Avah-Dickinson.user                                                                                          
-rw-rw-r-- 1 cabox cabox   79 Apr  6 19:20 Ayaan-Stiedemann.user                                                                                        
-rw-rw-r-- 1 cabox cabox   79 Apr  6 19:20 Aylin-Grant.user                                                                                             
-rw-rw-r-- 1 cabox cabox   70 Apr  6 19:20 Bedford-Sipes.user                                                                                           
-rw-rw-r-- 1 cabox cabox   82 Apr  6 19:20 Benita-King.user                                                                                             
-rw-rw-r-- 1 cabox cabox   92 Apr  6 19:20 Benito-Stoltenberg.user                                                                                      
-rw-rw-r-- 1 cabox cabox   83 Apr  6 19:20 Beverlee-Moen.user                                                                                           
-rw-rw-r-- 1 cabox cabox   76 Apr  6 19:20 Brad-Thiel.user                                                                                              
-rw-rw-r-- 1 cabox cabox   68 Apr  6 19:20 Brayan-Douglas.user                                                                                          
-rw-rw-r-- 1 cabox cabox   80 Apr  6 19:20 Bria-Satterfield.user                                                                                        
-rw-rw-r-- 1 cabox cabox   70 Apr  6 19:20 Bridgette-Reichel.user                                                                                       
-rw-rw-r-- 1 cabox cabox   78 Apr  6 19:20 Britt-Erdman.user                                                                                            
-rw-rw-r-- 1 cabox cabox   66 Apr  6 19:20 Britta-Hammes.user                                                                                           
-rw-rw-r-- 1 cabox cabox   68 Apr  6 19:20 Bryant-Kuhic.user                                                                                            
-rw-rw-r-- 1 cabox cabox   86 Apr  6 19:20 Bryton-Aufderhar.user                                                                                        
-rw-rw-r-- 1 cabox cabox   82 Apr  6 19:20 Caitlin-Grady.user                                                                                           
-rw-rw-r-- 1 cabox cabox   99 Apr  6 19:20 Carroll-Hartmann.user                                                                                        
-rw-rw-r-- 1 cabox cabox   80 Apr  6 19:20 Claudie-McClure.user                                                                                         
-rw-rw-r-- 1 cabox cabox   72 Apr  6 19:20 Clemente-Haley.user                                                                                          
-rw-rw-r-- 1 cabox cabox   84 Apr  6 19:20 Cleo-VonRueden.user                                                                                          
-rw-rw-r-- 1 cabox cabox   89 Apr  6 19:20 Codie-Romaguera.user                                                                                         
-rw-rw-r-- 1 cabox cabox   73 Apr  6 19:20 Cooper-Reynolds.user                                                                                         
-rw-rw-r-- 1 cabox cabox   80 Apr  6 19:20 Corrie-Bogisich.user                                                                                         
-rw-rw-r-- 1 cabox cabox   57 Apr  6 19:20 Dannielle-Green.user                                                                                         
-rw-rw-r-- 1 cabox cabox   86 Apr  6 19:20 Deedee-Jacobson.user                                                                                         
-rw-rw-r-- 1 cabox cabox   72 Apr  6 19:20 Desiree-Marks.user                                                                                           
-rw-rw-r-- 1 cabox cabox   64 Apr  6 19:20 Deven-Rutherford.user                                                                                        
-rw-rw-r-- 1 cabox cabox   80 Apr  6 19:20 Doyle-Jones.user                                                                                             
-rw-rw-r-- 1 cabox cabox   78 Apr  6 19:20 Dustyn-O'Connell.user                                                                                        
-rw-rw-r-- 1 cabox cabox   87 Apr  6 19:20 Elza-Mraz.user                                                                                               
-rw-rw-r-- 1 cabox cabox   67 Apr  6 19:20 Emory-Crona.user                                                                                             
-rw-rw-r-- 1 cabox cabox   79 Apr  6 19:20 Erin-Walker.user                                                                                             
--More--    


* Earlier, when you viewed the list of active processes on your devbox using `ps aux`, the list was probably really long. You can make this list more manageable by using the pipe (`|`) to filter the results of `ps` using `grep`. Run `ps aux | grep <your_username>` to see what processes are running for your specific user. *Paste the list of processes that reference your username here:*

root       507  0.0  0.6  63876  3308 ?        Ss   02:03   0:00 sshd: cabox [priv]                                                                     
cabox      509  0.0  0.2  64008  1500 ?        S    02:03   0:00 sshd: cabox@notty                                                                      
cabox      510  0.0  0.1  12776   840 ?        Ss   02:03   0:00 /usr/lib/openssh/sftp-server                                                           
root       561  0.0  0.6  63876  3456 ?        Ss   02:09   0:00 sshd: cabox [priv]                                                                     
cabox      563  0.0  0.2  63876  1468 ?        S    02:09   0:00 sshd: cabox@pts/0                                                                      
cabox      564  0.0  0.3  18128  2020 pts/0    Ss   02:09   0:00 -bash                                                                                  
cabox      577  0.0  0.2  15520  1148 pts/0    R+   02:11   0:00 ps aux                                                                                 
cabox      578  0.0  0.1   8816   744 pts/0    S+   02:11   0:00 grep --color=auto cabox
