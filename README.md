# Dotfiles

My configuration files for bash, vim, tmux and so forth.

## Setup Notes

The intention is to be able to run a setup script after cloning the repo on an Ubuntu system and be up and running very quickly.

### Ubuntu

```bash
DOTFILES_DIR=$HOME/dev/repos/github.com/bde-dev
mkdir -p $DOTFILES_DIR
cd $DOTFILES_DIR
git clone https://github.com/bde-dev/dotfiles.git
cd dotfiles
./setup

# Optionally descend into "tools" and install common CLI programs.
cd tools
./setup
```

### Windows and WSL setup

- Install WSL in powershell

```bash
The above command only works if WSL is not installed at all, if you run wsl --install and see the WSL help text, please try running wsl --list --online to see a list of available distros and run wsl --install -d <DistroName> to install a distro. To uninstall WSL, see Uninstall legacy version of WSL or unregister or uninstall a Linux distribution.
```

- Use [chocolatey](https://chocolatey.org/install) to install Windows Terminal Preview using `choco install microsoft-windows-terminal --pre`
- Get gruvbox-material color scheme for Windows Terminal.
- Open the settings.json in windows preview by opening a new tab and click on Settings while holding shift
- Paste in the colorschemes and asssign it to the Ubuntu profile in Windows Terminal

There is an issue with npm on wsl ubuntu 22. Use this to install npm: <https://stackoverflow.com/questions/73673804/npm-show-npm-elf-not-found-error-in-wsl>
