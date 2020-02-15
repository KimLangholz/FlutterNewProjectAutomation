# Flutter Github Initialization Automation

This is a automation script that in its current form does the following for you when you run this command:
```
create new_project_name
```
* Creates a new GitHub Repository.
* Creates a new Flutter project in a pre-determined location.
* Runs the following sequence:

```
git init
git remote add origin //LOCATION
git add .
git commit -m "Initial commit"
git push -u origin master
```
* Opens the project in VSCODE. 

## Initial Setup

* Clone project to your computer.
* Create a .env file and copy .env.example into it.
* Add your own [GitHub accesstoken] (https://github.com/settings/tokens) to the .env file
* Replace line 5 and 7 in create_repo.sh with your desired project path location. *The path on line 7 needs to end with $1*
* Replace the GitHub accountname in the GitHub URL with your own GitHub account name. 

### MacOS specific Setup

**For zsh users** 
Add: alias create="/Users/kimlangholz/Projects/Python/ProjectInitializationAutomation/create_repo.sh" to your .zshrc file in your HOME folder. Obviously changing the path to reference your local create_repo.sh file.

**For bash users**
Add: alias create="/Users/kimlangholz/Projects/Python/ProjectInitializationAutomation/create_repo.sh" to your .bash_profile file in your HOME folder. Obviously changing the path to reference your local create_repo.sh file.


### Roadmap

 [ ] Write a guide for using this on Windows and Linux
 [ ] Add options when creating a Flutter project based on several pre-defined templates.

###### Credits

*This project was inspired by [this video](https://www.youtube.com/watch?v=7Y8Ppin12r4) made by [KalleHalden](https://github.com/KalleHallden/ProjectInitializationAutomation)*