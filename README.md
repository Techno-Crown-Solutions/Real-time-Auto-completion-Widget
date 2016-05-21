# Real-time Auto-completion Widget
“Real-Time Auto-Completion Widget” is designed for Debian based OS like Ubuntu. It has two new features in **real-time** alongside bash terminal:
- **Displaying possible matches**
![Screenshot 1](https://github.com/Techno-Crown-Solutions/Real-time-Auto-completion-Widget/blob/master/screenshots/Auto-completion-widget-apt-screenshot-1.jpg "AC widget displaying possible matches for apt-")

- **Man Page**
![Screenshot 2](https://github.com/Techno-Crown-Solutions/Real-time-Auto-completion-Widget/blob/master/screenshots/Auto-completion-widget-apt-get-screenshot-2.jpg "AC widget displaying man page")

This widget displays the completion of commands in set of 24 possibilities, and man pages on a scrollable window in two cases: 
- When a command is completed on a terminal
- When button on widget is clicked.
 
It also has a ‘lock’ button with which one can save the state of widget and refer this state while working in terminal. This widget is recommended for the new Linux users and those who are not familiar with terminal, so that they can overcome the complexities working with commands. Currently, it works perfectly on Ubuntu 15.10 .



### Dependency
You need Gtk+ developer tools to compile and run the source. You can get it by running the below command.
```sh
sudo apt-get install libgtk-3-dev
```


### Installation:
-	Download  [bash-4.3.30.tar.gz](https://ftp.gnu.org/gnu/bash/bash-4.3.30.tar.gz) and place in home directory.
-	Unzip the *bash-4.3.30.tar.gz* by command `tar –zxvf  bash-4.3.30.tar.gz`
-	Change directory to bash-4.3.30/ by `cd bash-4.3.30/`
-	Download the **readline.h** , **complete.c** and **text.c** and copy these files to `bash-4.3.30/lib/readline` folder.
-	Open the **complete.c** and change the `user-name` to your name in line numbers *2083, 2084, 2163* and *2164*.
-	Configure and create *make* file using command below.
```sh 
./configure --prefix=/user –bindir=/bin 
```
- Compile the *bash*.
```sh
sudo make
```
-  Install modified *bash*.
```sh
sudo make install (ignore errors)
```
-  Change to the new compiled bash.
```sh
exec bash
```
-  Copy the downloaded **gui2 .py**, **vfifo3 .py** and **acwidget .py** to home directory.





## Running the widget:
Open a new terminal and run the command 
```sh
python acwidget.py
```
Then type in the other terminal to get the possibilities and man page.



#### Developed by
##### [Techno Crown Solutions](http://techno-crown.com) ( Varun Sharma N and Karthik Prabhu )
###### For any support or feedback, contact us at technocrowns@gmail.com , varun15sharma15@gmail.com , karthik.prabhu55@gmail.com
