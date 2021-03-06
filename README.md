Project - Mini-Shell
---------------------

Introduction:
-------------
Implement a minimalistic shell, mini-shell(msh) as part of the Linux Internal module.
The objective is to understand and use the system calls w.r.t process creation,
signal handling, process synchrnonization, exit status, text parsing etc..

Requirements list:
------------------
+ Provide a prompt for the user to enter commands
  > Display the default prompt as msh>
  > Prompt should be customizable using environmental variable PS1
    - To change the prompt user will do PS1=NEW_PROMPT
    - Make sure that you do not allow whitespaces between =
      i.e., do not allow PS1   =  NEW_PROMPT
    - In the above case, it should be treated like a normal command

+ Execute the command entered by the user
  > User will enter a command to execute
  > If it is an external command
    - Create a child process and execute the command
    - Parent should wait for the child to complete
    - Only on completion, msh prompt should be displayed

Special Variables:
------------------
+ Exit status of the last command (echo $?)
  > After executing a command the exit status should be available
  > echo $? should print the exit status of the last command executed

+ PID of msh (echo $$)
  > echo $$: should print msh's PID

+ Shell name (echo $SHELL)
  > echo $SHELL: should print msh executable path

Signal handling:
----------------
Provide short cuts to send signals to running program

Ctrl-C (Send SIGINT)
--------------------
+ On pressing Ctrl-C
  > If a programming is running in foreground, send SIGINT to the progam (child process)
  > If no foreground program exists, re-display the msh prompt


Built-in commands
------------------
+ exit
  > exit: This command will terminate the msh program


Design:
-------
You should write down the how your are going to implement the project.
You have to think through the design, then write down a detailed description
of the design. Use diagram like flowchart to give clarity. Write down the algorithm/pseudo-code
as appropriate.

