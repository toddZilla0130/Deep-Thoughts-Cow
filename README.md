## Introduction
blah blah blah "stuff."

## Prereqs
### Download and install `fortune` and `cowsay` for your platform:
#### Ubuntu/Debian
```shell
sudo apt update && sudo apt install cowsay fortune -y
```
#### CentOS/RHEL/SUSE
```shell
sudo yum update && sudo yum install cowsay fortune -y ## need to confirm this!
```
#### MacOS
```shell
brew update
brew install fortune cowsay ## need to confirm this!
```
#### WSL (Windows Subsystem for Linux)
Follow the directions above for the appropriate distro you have installed.

### Confirm successful install
(TODO)

## Clone the repo
```shell
cd ~
mkdir jackhandy
cd jackhandy
git clone...
```

(TODO)

## Configure (by **shell**)

### `zsh+oh-my-zsh`
This has been tested with MacOS, Ubuntu, CentOS (not really, at least not yet), and WSL.

`cd` into `~/.oh-my-zsh/custom`

`oh-my-zsh` runs each of the files in this subdir when you open a new terminal window. To include the `deepthoughts` script, type this at the command prompt:

```shell
ln -s ~/jackhandy/deepthoughts deepthoughts.zsh
```
Replace `jackhandy` in the filepath with ...

You do not have to `chmod` the script to be executable; you _do_, however, need to include the `.zsh` extension on the alias.

Remember that `oh-my-zsh` executes the files in this directory in canonical order. If you print other stuff to the terminal during startup and want the cow to appear immediately above the command prompt, consider prepending the file name to force it to run last, e.g. `z-deepthoughts.zsh`.

For (the unbeatable combo of) `zsh` and `oh-my-zsh` that's it! The next time you open a terminal window (or `source .zshrc`) you should see the Deep Thought Cow.

### `zsh` (without `oh-my-zsh`) and `bash`
(TODO: same-ish as above but different.)

```
Your Deep Thought for this session:
 ________________________________________
/ The face of a child can say it all,    \
\ especially the mouth part of the face. /
 ----------------------------------------
        \   ^__^
         \  (OO)\_______
            (__)\       )\/\
                ||----w |
                ||     ||
```