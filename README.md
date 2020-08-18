## Introduction
blah blah blah "stuff."

## Prereqs
### Download and install `fortune` and `cowsay` for your platform:
#### Ubuntu/Debian/WSL
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

### Confirm successful install
(TODO)

## Clone the repo
(TODO)

## Configure (by *shell*)

### `zsh+oh-my-zsh`
`cd` into `~/.zshrc/custom`
Open your favorite editor and paste these lines:
```shell
#! /usr/bin/zsh

echo
opts=(b d g p s t w y) # cow face option
opt=${opts[$RANDOM%${#opts[@]}+1]}    # choose a random one. NOTE: The array is 1-based.
echo "Your Deep Thought for this session:"
fortune /path/to/jackhandy | cowsay -$opt
echo
```

Save it to whatever file name you'd like. It doesn't need an extension; nor is it mandatory to `chmod` it as an executable. 

Remember that `oh-my-zsh` executes the files in this directory in canonical order. If you print other stuff to the terminal during startup and want the cow to appear immediately above the command prompt consider prepending the file name to force it to run last, e.g. `z-deepthoughts`.