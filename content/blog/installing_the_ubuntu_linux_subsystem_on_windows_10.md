
+++
author = "Caleb Faught"
categories = ["Operating Systems", "Linux", "Windows"]
date = "2017-02-19"
description = "Adding a Linux Subsystem to Windows 10"
featured = "pic1.jpg"
featuredalt = "Ubuntu and Windows logos"
featuredpath = "date"
linktitle = ""
title = "Installing the ubuntu linux subsystem on windows 10"
type = "post"

+++

I recently had the pleasure of restoring my Windows laptop after breaking something in a Linux dualboot (another story for another day). While going through all the process of setting things back up, I remembered that I had heard somewhere that Windows 10 now has the capability for developers to install a full Ubuntu environment within Windows (No Virtual Machine Required). This enables users to open a Bash shell and run Linux tools all without loading a VM or rebooting. After doing some Googling and trying some things, I figured I would compile my install experience in one place for anyone interested.

# Prerequisites
* A 64-bit PC running a 64-bit version of Windows 10 (fully up to date).

# Enable Bash on Ubuntu on Windows 10
* First enable Developer mode in Windows: `Settings > Update & Security > For Developers > Developer Mode` (You may be prompted for permission to continue, and possibly reboot).
* Search `Turn Windows Features On or Off` in the taskbar search field.
* Look for an entry for `Windows Subsystem for Linux (Beta)`, and tick the checkbox.
* Click OK, and now reboot your computer.
* Once Windows is back up and running, search `Bash` in the taskbar search field and you should see Bash with the Ubuntu logo come up as the first entry; click this to launch a Bash shell. (Also right click and add to taskbar is helpful).

# Installing Ruby on Rails
* Open Bash and update apt: `sudo apt-get update`
* Next run:
```
sudo apt-get install git-core curl zlib1g-dev build-essential libssl-dev libreadline-dev libyaml-dev libsqlite3-dev sqlite3 libxml2-dev libxslt1-dev libcurl4-openssl-dev python-software-properties libffi-dev
```
* I'm using RVM for managing Ruby so, install that next:
```
sudo apt-get install libgdbm-dev libncurses5-dev automake libtool bison libffi-dev
gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3
curl -sSL https://get.rvm.io | bash -s stable
echo '[[ -s "$HOME/.rvm/scripts/rvm" ]] && source "$HOME/.rvm/scripts/rvm"' >> .bashrc
source ~/.rvm/scripts/rvm
rvm install 2.4.0
rvm use 2.4.0 --default
gem install bundler
```
* Install Node.js:
```curl -sL https://deb.nodesource.com/setup_4.x | sudo -E bash -
sudo apt-get install -y nodejs
```
* And finally install Rails: `gem install rails -v 5.0.1`
* Optionally I installed Postgres (For Heroku) on Windows, and the Bash environment is able to connect and talk to the Windows installation of Postgres (Not sure how this works quite yet, but I assume its built-in by Microsoft).


# Set up Git (optional I guess?)
```
git config --global color.ui true
git config --global user.name "YOUR NAME"
git config --global user.email "YOUR@EMAIL.com"
ssh-keygen -t rsa -b 4096 -C "YOUR@EMAIL.com"
```
* Now Run `cat ~/.ssh/id_rsa.pub` and copy the output.
* Create a new ssh key on [Github](https://github.com/settings/keys) and paste the key where prompted.



# Things to be Aware of
* Running graphical applications is not intuitive. I have tried installing Atom Editor with little luck. However, console applications work great!
* **Do not try editing Windows files from Bash/Ubuntu!**

# In Conclusion
I think this is an interesting idea. Especially now that I am focusing on learning C# after my Ruby on Rails/Javascript oriented bootcamp experience (Shout out to [Flatiron School](http://flatironschool.com)). Now I am able to potentially work on Rails projects using the same great tools I use in Linux, and also use things like Visual Studio for C# development on one system. There are some limitations, some of which I have mentioned, but I hope that Microsoft continues to develop this environment. In the end I'll probably have an Ubuntu VM since I like playing with Linux anyways.
