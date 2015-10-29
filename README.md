# bigsqlrunner

Cloned from
http://bigsqlrunner.codeplex.com/


# Project Description
In the real world application, for database developers or database system administrator or others, they can encounter the case: "Backup database without using .bak files". As usual, they will open the sql script file and run it directly inside Sql Server Management Studio(SSMS) tool or via command line. For <= 300MB sql script files, SSMS can do this for you easily and reliably. But for > 300MB these sql script files, SSMS can't open and run it directly. Even though so, there is an useful utility called "sqlcmd" can do this for you. However, sqlcmd tool doesn't support to rollback and stop&continue running the script files. From disadvantage points, I had a good idea to do this by developing a tool to run these sql script files for any size. This tool is called BigRunner. It consists of these following features:

    Run the sql script file for any given size.
    Enable log the running status to file.
    Support both command line and graphic user interface(GUI).
    Support rollback the running script (in the next release).
    Support stop & continue running script (in the next release). 

# Usage
BigRunner supports two user interfaces: command line and GUI. For command line, you click into BigRunnerCmd.exe executable file and input these necessary data and run it. For GUI, you also do same as for command line instead of clicking BigRunnerGui.exe executable file.

# Requirements

You have to meet the following requirements before running the program:

    Install .Net Framework 4.0 or later if not having on your machine.
    If you run the sql script file directly on your database server on your machine, please make sure that you must install Sql Server on it.
    Your t-sql script in the file have to be separated by GO batch. 

# Examples
Exp1) We will backup 1 database called Test. This database is in empty status. As assumed that we had the backup data in the sql script files about more than 2GB. We will demonstrate and do this by using BigRunnerCmd.exe:

Step 1: download file BigRunnerCmd.exe from this page at Downloads section.

Step 2: Double-click at this file.

Step 3: This console program is shown as follows:

Step 4: you enter the valid connection string based upon example connection string as above. Here's my valid connection string at my local point to the database called "Test". Then, press Enter to continue

Step 5: Input the big script file full path on your hard drive. Here's my local file path and press Enter to continue

Step 6: Enable log the running status to file if you input "yes" value. Otherwise input "no" to continue. In this case, I will input "yes" to write log to the file and press Enter to continue:

Step 7: Input the full file path to write the log. If this file doesn't exist, the program will automatically create it for you. Otherwise, it will get this file for logging. Here's my existed log file path

Step 8: you can wait until running completely. In additional, in order to stop running, you press any key to do this. Here I pressed "r" key to cancel running.

Step 9: you press Esc key to exit console program.

# Last Step: open SSMS tool and view the results.

Exp 2) You also do this like as Exp 1) except for that I demonstrate on graphic user interface

Step 1: you download BigRunnerGui.exe from Downloads section.

Step 2: you double-click into this file to run it.

Step 3: you input these necessary data like as Exp 1) on GUI as follows

Step 4: click Run button to run the sql script

Step 5: this step is like as step 8 at Exp 1) instead of GUI

Last step: exit GUI and then open SSMS and view the results.

# Certification
