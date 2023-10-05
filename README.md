# :page_facing_up: dotfiles & Scripts

i'm a nerd :nerd_face:

## justfile

i have some commands
check with

```sh
    just
```

## Scripts

### Windows: Create folder backup

useful script for backing up folders

(optional): create `.backupignore` file:

```plaintext
folder1\
folder2\
config.ini
```

1. create a environment variable `BACKUP`
2. create script for backing up:

```powershell
iwr $env:USERPROFILE/scripts/create-folder-backup.ps1 | iex
```

## Remote Scripts

I have some scripts that can be used remotely

### Windows: Setup

```powershell
&powershell -NoProfile -ExecutionPolicy unrestricted -Command "&([scriptblock]::Create((Invoke-WebRequest -UseBasicParsing 'https://raw.githubusercontent.com/cethien/dotfiles-and-scripts/win/scripts/setup.ps1'))) <parameters>"
```

| Parameter    | Description                             |
| ------------ | --------------------------------------- |
| -Customizing | customization stuff                     |
| -Personal    | some stuff on a personal desktop        |
| -Ssh         | generate a new ssh key. uses ssh-keygen |
| -Development | development stuff                       |
| -Gaming      | games & launchers                       |
| -Streaming   | streaming stuff                         |

### Debian: Setup

```bash
    curl -fs https://raw.githubusercontent.com/cethien/dotfiles-and-scripts/wsl-deb/scripts/setup.sh | bash -s
```
