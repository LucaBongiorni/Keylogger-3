# Keylogger for Windows and Mac
## Windows
Simply compile into an .exe, and then run. 

There are two files; klog_visible and klog_invisible. It is pretty simple, but I will expand:

`klog_visible` is visible, and the window does not close when typing. Great for testing it out. `klog_invisible` makes the window of the logger disappear, and it also starts up hidden from view. Note that it is still visible in the task manager.

Both of these save the keystrokes to a .txt file when closed.

## Mac
This is a little more complicated, as its Apple after all! Please note, it does not work for secure areas such as password inputs. I have not found a work around yet.

### Installation
Download the repo. It will install in `/usr/local/bin/keylogger`.

Install it:

`$ git clone https://github.com/GiacomoLaw/Keylogger && cd keylogger
$ make && make install`

It will log to `/var/log/keystroke.log`. This may require root access, but you can change that if you want. Set where you want it to log:

`$ keylogger ~/logfile.txt
Logging to: /var/log/keystroke.log`

Want to make it start on system startup?

`$ sudo make uninstall`

That will run it on startup.

### Uninstall
`$ sudo make uninstall`
Will uninstall the program, but not the logs.

---

Please feel free to contribute to fix any problems, or to submit an issue!

Please note, this repo is for educational purposes only. No contributors are to fault for any actions done by this program.
