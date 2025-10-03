# git-profile

Manage multiple git identities per repository.

## What it does

Switches between predefined git user profiles on a per-repository basis. Useful when you commit to personal projects, work repositories, and open source under different identities.

## Installation

```bash
git clone https://github.com/tiefpunkt/git-profile.git
cd git-profile
sudo cp git-profile /usr/local/bin/
sudo chmod +x /usr/local/bin/git-profile
```

Configure git to require explicit identity:

```bash
git config --global user.useConfigOnly true
git config --global --unset-all user.email
```

## Configuration

Create `~/.gitprofile` with your profiles:

```ini
[personal]
name = John Doe
email = john@doe.net

[work]
name = John Doe
email = john.doe@work.com
```

## Usage

List available profiles:

```bash
git profile list
```

Set profile for current repository:

```bash
git profile use personal
```

After setting a profile, commits will use that identity:

```bash
git commit -m "initial commit"
```

## Uninstall

```bash
sudo rm /usr/local/bin/git-profile
```

## Alternatives

- [git-profiles](https://github.com/bddenhartog/git-profiles)
- [multiple-git-identities](https://maarten.mulders.it/2020/07/multiple-git-identities/) (conditional includes approach)
- [Can I specify multiple users for myself in gitconfig?](http://stackoverflow.com/questions/4220416/can-i-specify-multiple-users-for-myself-in-gitconfig)
