# git-profile
Manage multiple identity profiles for git commits.

## Setup

```
git clone https://github.com/tiefpunkt/git-profile.git
cd git-profile
sudo cp git-profile /usr/local/bin/
sudo chmod +x /usr/local/bin/git-profile
git config --global user.useConfigOnly true
git config --global --unset-all user.email
```

## Usage
```
severin@thingie:~/devel/git-profile$ git commit -m "initial commit"

*** Please tell me who you are.

Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.

fatal: no email was given and auto-detection is disabled

severin@thingie:~/devel/git-profile$ git profile use personal
Set user to Severin Schols <severin@schols.de>

severin@thingie:~/devel/git-profile$ git commit -m "initial commit"
[master (root-commit) d1fdc6a] initial commit
 2 files changed, 37 insertions(+)
 create mode 100644 README.md
 create mode 100755 git-profile
```

## Other projects and approaches

* https://github.com/bddenhartog/git-profiles
* http://stackoverflow.com/questions/4220416/can-i-specify-multiple-users-for-myself-in-gitconfig
* https://orrsella.com/2013/08/10/git-using-different-user-emails-for-different-repositories/
