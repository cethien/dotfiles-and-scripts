# :page_facing_up: dotfiles & Scripts

i'm a nerd :nerd_face:

## Stuff

### justfiles

each home dir has a justfile.

Check out list of commands with:

```sh
just
```

## Windows

### Update

prepare `.wingetupdate` file

```powershell
. "$env:USERPROFILE/scripts/update.ps1"
```

### Setup

```powershell
git init
git remote add origin https://github.com/cethien/dotfiles-and-scripts.git
git fetch
git reset --hard origin/win
git pull --set-upstream origin win
```

```powershell
. "$env:USERPROFILE/scripts/setup.ps1" <parmeters>
```

| Parameter    | Description                             |
| ------------ | --------------------------------------- |
| -Customizing | customization stuff                     |
| -Personal    | some stuff on a personal desktop        |
| -Ssh         | generate a new ssh key. uses ssh-keygen |
| -Development | development stuff                       |
| -Gaming      | games & launchers                       |
| -Streaming   | streaming stuff                         |

### Create folder backup

useful script for backing up folders

1. create a environment variable `BACKUP`
2. create script for backing up:

```powershell
. $env:USERPROFILE/scripts/create-folder-backup.ps1
```

(optional): create `.backupignore` file:

```plaintext
folder1\
folder2\
config.ini
```

## WSL Debian

### Setup

```bash
git init
git remote add origin https://github.com/cethien/dotfiles-and-scripts.git
git fetch
git reset --hard origin/wsl-deb
git pull --set-upstream origin wsl-deb
```

```powershell
. ~/scripts/setup.sh
```
