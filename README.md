# :page_facing_up: dotfiles & Scripts

i'm a nerd :nerd_face:

## Commands

| OS    | Command          | Description                            |
| ----- | ---------------- | -------------------------------------- |
| 🪟 🐧 | `reload`         | reloads shell profile                  |
| 🪟 🐧 | `update`         | execute package/app updates            |
| 🪟    | `update-spotify` | update spicetify                       |
| 🐧    | `update-dotnet`  | update dotnet sdk version to 'latest'  |
| 🐧    | `update-go`      | update go sdk version to 'latest'      |
| 🐧    | `init-go-web`    | creates a go web project from template |
| 🐧    | `init-go-web`    | creates a go web project from template |

## Git

| Type    | Command      | Description/Value                                 |
| ------- | ------------ | ------------------------------------------------- |
| command | `git ignore` | fetches ignore file: `git ignore go > .gitignore` |
| alias   | `ga`         | `git add`                                         |
| alias   | `gaf`        | `git add -f`                                      |
| alias   | `gc`         | `git commit -m`                                   |
| alias   | `gf`         | `git fetch`                                       |
| alias   | `gr`         | `git reset --hard`                                |

## Scripts

### Setup (Windows)

```powershell
git init
git remote add origin https://github.com/cethien/dotfiles-and-scripts.git
git fetch
git reset --hard origin/win
git pull --set-upstream origin win

. "$env:USERPROFILE/scripts/setup.ps1" -Profiles <profiles>
```

| Profile       | Description                      |
| ------------- | -------------------------------- |
| `customizing` | customization stuff              |
| `home`        | some stuff on a personal desktop |
| `dev`         | development stuff                |
| `gaming`      | games & launchers                |

### Setup (WSL Ubuntu/Debian)

```bash
git init -b wsl-deb
git remote add origin https://github.com/cethien/dotfiles-and-scripts.git
git fetch
git reset --hard origin/wsl-deb
git pull --set-upstream origin wsl-deb

. $HOME/scripts/setup.sh
```

dont forget to set git username and email for repo!

### Create folder backup (Windows)

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
