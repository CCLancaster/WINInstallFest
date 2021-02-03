# Windows 10 OS

## Windows Install Fest

## Part 1 

For the first portion of the installfest, we'll be working exclusively inside of the browser. We'll be installing the following tools:
Slack
Git
Node.js
VS Code


### Slack

We will be using slack to communicate throughout the course. You should've received an invite to our channels via e-mail. You can login via the web browser, but downloading / installing the app is highly recommended.

[Download Slack](https://slack.com/downloads/windows)

### GIT

#### Download/Install GIT

[Download GIT](https://git-scm.com/downloads) 

Launch Git Installer, allow the app to make changes on your device, use default settings unless you have a different preference.

For step by step instructions see [this article](https://phoenixnap.com/kb/how-to-install-git-windows)

#### Configuring GIT

Using your email credentials for GitHub, run these commands with your user and email configured.

    git config --global user.name "YOUR-USERNAME"
    git config --global user.email "YOUR-EMAIL-ADDRESS"
    git config --global push.default simple
    git config --global credential.helper cache

Setting up SSH Key

You might find your self having to re-authenticate GIT every time you work on your command line. Setup SSH Keys to let Github remember your machine in the future.

* [Github Generating SSH Keys](https://docs.github.com/en/free-pro-team@latest/github/authenticating-to-github/connecting-to-github-with-ssh)


###  Node

To install Node

* [Node.js](https://nodejs.org/en/)
Select the LTS version, this is recommended for most users.

![](/images/node.png)


### Install VS Code

Currently the most popular editor according to developer polls. This is Microsoft's free version of Visual Studio.

Download and install VS Code from here

You're all good to go now, but for ease of use, let's make it so we cna automatically open up any file or project in VS Code, from our command line. The following instructions are taken from these docs. If you're on a Windows or linux, see the left-side menu to switch to the instructions for your machine.

To be able to open VS Code from any directory, open the Command Palette (Shift+⌘+P) and type 'shell command' to find the Shell Command: Install 'code' command in PATH command (it will be the first one that comes up).

Restart the terminal for the new $PATH value to take effect. You'll be able to type 'code .' in any folder to start editing files in that folder.


## Part 2

This next part will be mostly done in your systems on your machine. We will be doing the following: 

Enabling Microsoft Developer
Ububtu 

### Enable Windows Developer Mode
Begin by going into the developer setting.

![Developer Settings](/images/devsetting.png)

#### Once inside turn developer setting on as well as Powershell

![](/images/devmode.png)
![](/images/enable1.png)
![](/images/enable2.png)

### Enable Subsystem for Linux

Press the windows key + R to open the run controller.

Type `optionalfeatures.exe` in the popup.

![](/images/step2.png)

This new window you will need to scroll down to the `Windows Subsystem for Linux`

![](/images/opfeatures.png)

Press ok and PUSH and update for Windows.
*Windows might not ask you to update at the time, however you need to check for an update.

 **Restart your windows machine**

**Once your machine has restarted**

Open the windows App store and search for seach and install Ubuntu.


![](/images/ubuntu.png)


After this has been installed open and run the ubuntu terminal install

![](/images/ubunturun.png)


**You do _NOT_ need to make an account once it has been installed**

Close Ubuntu. This will be the last time we use Ububtu.

### Adding `Touch` to the Powershell commands
Copy and paste this code chunk into the Powershell terminal.

    function touch {New-Item -ItemType File -Name ($args[0])}


