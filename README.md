# ASSIGNMENT REMINDER APP
Table of contents
Creating the application work space
Checking for students submission status
The assignment reminder app is a basic app that basically helps you to the students' submission status for various assignments. 

## How does this application work?
### Creating the environment
The first step that you take is to create the application environment.
To do that, you simply run the ***==create_environment.sh==*** file either through ==./create_environment.sh== or ==bash create_environment.sh.== While creating the directory structure, you will be prompted to input your name. The purpose for inputting your name is so that when the parent directory of your application is being created, it can have your name at the end. This makes it easy for  you to identify your directory that has your students' information.
After running the ***==create_environment.sh==*** file, your directory structure must look like the one shown below.

## submission_reminder_app(name)
```bash
.
├── app
│   └── reminder.sh
├── assets
│   └── submissions.txt
├── config
│   └── config.env
├── modules
│   └── functions.sh
└── startup.sh
```

### Checking students' submission status.
The next simple step after creating your application work space is to check your students submission status. To achieve this, you have to simply run the ***==copilot_shell_script.sh==*** through either typing `==./copilot_shell_script.sh==` or `==bash copilot_shell_script.sh.==`
The first thing that happens is you are shown an interactive menu with all the assignments on it that you can check. After that, you have to put in your choice, and then the student's submission status is shown. You are then again asked if you want to check another assignment. This keeps on happening in a loop until you choose to exit.

## The core knowledge behind assignment status check.
When you chose an assignment that you want to check the students submission status, The name of the assignment is then used as the string for the variable named ASSIGNMENT in the file config.env, which is located in config/ directory in submission_riminder_(name) parent directory.
After successfully replacing the assignment, the **==startup.sh==** file which is also found in the ==submission_reminder_(name)== directory is then executed.
The ==startup.sh== file then executes  ‘==./app/reminder.sh‘== file that is also in the **==submission_reminder_(name)==** parent directory. 
The ==./app/reminder.sh== file then prints the assignment name and the number of days left to the deadline. The ==./app/reminder.sh ==file also executes ==./modules/functions.sh== file. This file contains scripts that will check for students submission status in ==./assets/submission.txt== file, then print those who haven’t submitted their assignments for the very assignment that we are checking.
