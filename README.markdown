Setting up a new macOS computer
===============================

The initial software and code setup for my personal computers,
for use with [suited](https://github.com/norm/suited).


## macOS account setup

During the installation of macOS

* don't sign into iCloud during the finalisation
* create alternate `king` account, not `norm`

Once logged in, open System Preferences and:

* create the `norm` account
* turn off fast user switching
* set the login window to display as "Name and password"
* change the hostname in the Sharing pane

Log out, then back in as `norm`, signing into iCloud during the finalisation.


## Terminal preferences

```
(nohup sh -c 'sleep 10; cp ~/Library/Mobile\ Documents/com~apple~CloudDocs/kit/com.apple.Terminal.plist ~/Library/Preferences; say done' &) && kill -9 $$
```

## Software installation and environment customisation 

Copy your ssh key into place and activate it with `ssh-add`.

Explicitly sign into the Mac App Store application: Store → Sign In… 

Run suited:

```
export GITHUB_TOKEN=____TOKEN_GOES_HERE____
export GITHUB_USER='norm'
export GIT_EMAIL='norm@201created.com'
export GIT_NAME='Mark Norman Francis'
export HOST=`hostname -s`
curl -O https://raw.githubusercontent.com/norm/suited/master/suited.sh 
bash suited.sh github:norm/suit:main.conf
```

Reboot once suited has run successfully all the way through.
