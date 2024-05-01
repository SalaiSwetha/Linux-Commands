### Introduction to the Bash Shell
A command line is a text-based interface which can be used to input instructions to a computer
system. The Linux command line is provided by a program called the shell. Various options for the
shell program have been developed over the years, and different users can be configured to use
different shells. Most users, however, stick with the current default.<br>
The default shell for users in Red1Hat Enterprise1Linux is the GNU Bourne-Again Shell (bash).
Bash is an improved version of one of the most successful shells used on UNIX-like systems, the
Bourne Shell (sh).
When a shell is used interactively, it displays a string when it is waiting for a command from the
user. This is called the shell prompt. When a regular user starts a shell, the default prompt ends
with a $ character, as shown below.<br>
<b> [user@host ~]$ </b><br>
The $ character is replaced by a # character if the shell is running as the superuser, root. This
makes it more obvious that it is a superuser shell, which helps to avoid accidents and mistakes
which can affect the whole system. The superuser shell prompt is shown below.<br>
<b>[root@host ~]# </b> <br>
Using bash to execute commands can be powerful. The bash shell provides a scripting language
that can support automation of tasks. The shell has additional capabilities that can simplify or
make possible operations that are hard to accomplish efficiently with graphical tools.<br>
## Shell Basics
Commands entered at the shell prompt have three basic parts:<br>
<b>• Command to run</b><br>
<b>• Options to adjust the behavior of the command</b><br>
<b>• Arguments, which are typically targets of the command</b><br>
The <b>command</b> is the name of the program to run. It may be followed by one or more options, which
adjust the behavior of the command or what it will do.<br> <b>Options</b> normally start with one or two
dashes (-a or --all, for example) to distinguish them from arguments.<br> <b>Commands</b> may also
be followed by one or more arguments, which often indicate a target that the command should
operate upon.
For example, the command usermod -L user01 has a command (usermod), an option (-L),
and an argument (user01). The effect of this command is to lock the password of the user01
user account.

## Logging in over the Network

In Linux, the most common way to get a shell prompt on a remote system is to use Secure
Shell (SSH). Most Linux systems (including Red1Hat Enterprise1Linux) and macOS provide the
OpenSSH command-line program ssh for this purpose.<br>
In this example, a user with a shell prompt on the machine host uses ssh to log in to the remote
Linux system remotehost as the user remoteuser:<br>
<b>[user@host ~]$ ssh remoteuser@remotehost<br>
remoteuser@remotehost's password: password<br>
[remoteuser@remotehost ~]$</b><br>

The ssh command encrypts the connection to secure the communication against eavesdropping
or hijacking of the passwords and content.<br>
Some systems (such as new cloud instances) do not allow users to use a password to log in with
ssh for tighter security. An alternative way to authenticate to a remote machine without entering a
password is through public key authentication.<br>
With this authentication method, users have a special identity file containing a private key, which
is equivalent to a password, and which they keep secret. Their account on the server is configured
with a matching public key, which does not have to be secret. When logging in, users can configure
ssh to provide the private key and if their matching public key is installed in that account on that
remote server, it will log them in without asking for a password.<br>
## Logging Out
When you are finished using the shell and want to quit, you can choose one of several ways to end
the session. You can enter the exit command to terminate the current shell session. Alternatively,
finish a session by pressing Ctrl+D.
The following is an example of a user logging out of an SSH session:<br>
<b>[remoteuser@remotehost ~]$ exit<br>
logout<br>
Connection to remotehost closed.<br>
[user@host ~]$</b><br>

Basic Command Syntax<br>
<b>[user@host]$ whoami<br>
user<br>
[user@host]$</b><br>

The following example shows how to combine two commands (command1 and command2) on the
command line.<br>
<b>[user@host]$ command1;command2</b><br>

The <b>date</b> command displays the current date and time. It can also be used by the superuser to
set the system clock. An argument that begins with a plus sign (+) specifies a format string for the
date command.<br>
<img src="Linux Commands Date.png">




