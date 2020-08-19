### Introduction
blah blah blah "stuff."

### Prereqs
#### Download and install `fortune` and `cowsay` for your platform:
##### Ubuntu/Debian
```shell
sudo apt update && sudo apt install cowsay fortune -y
```
##### CentOS/RHEL/SUSE
```shell
sudo yum update && sudo yum install cowsay fortune
```
##### MacOS
```shell
brew update
brew install fortune cowsay ## need to confirm this!
```
##### WSL (Windows Subsystem for Linux)
Follow the directions above for the appropriate distro you have installed.

##### Other Linux distros
Man, you're on your own here. Please let me know the details and I'll update.

#### Confirm successful install
(TODO)

### Clone the repo

```shell
cd ~
mkdir jackhandy
cd jackhandy
git@github.com:toddZilla0130/Deep-Thoughts-Cow.git
```
You can call the directory anything you'd like - I call it **jackhandy** as he is the author of these gems. 

### Configure (by **shell**)

#### `zsh+oh-my-zsh`
This has been tested with MacOS, Ubuntu, CentOS (not really, at least not yet), and WSL.

`cd` into `~/.oh-my-zsh/custom`

**oh-my-zsh** runs each of the files in this subdir when you open a new terminal window. To include the `deepthoughts` script, type this at the command prompt:

```shell
ln -s ~/jackhandy/deepthoughts deepthoughts.zsh
```
If you opted for a different directory please make the appropriate substitution above.

You do not have to `chmod` the script to be executable; you _do_, however, need to include the `.zsh` extension on the alias.

Remember that `oh-my-zsh` executes the files in this directory in canonical order. If you print other stuff to the terminal during startup and want the cow to appear immediately above the command prompt, consider prepending the file name to force it to run last, e.g. `z-deepthoughts.zsh`.

For (the unbeatable combo of) `zsh` and `oh-my-zsh` that's it! The next time you open a terminal window (or `source .zshrc`) you should see the Deep Thought Cow.

#### `zsh` (without `oh-my-zsh`) 
(Make the script file executable, add running it to .zshrc)

#### `bash`
(Same as above, but need to change the `#!` line; add to .bashrc.)

#### Other shells
As I wrote above, you're on your own but if you're using a different shell you probably know a lot more about Linux than I do. I'll be happy to update here if you want to provide me with details.

## About the jackhandy file
It's a set of Deep Thoughts I culled/scraped from collections around the internet which _I_ think are funny. You may have a different opinion; if so I highly encourage you to edit the file to make it your own. Google "Deep Thoughts" or "Jack Handy" to start mining.

The file layout is simple:

```
Deep thought on a single line.
%
Another deep thought on a single line.
%

(etc.)
```

Save the file, then run 
```shell
strfile jackhandy
```
to regenerate the index (`.dat`) file.

If - like me - you're a bit anal retentive and like your Deep Thoughts sorted, you can run this command from the prompt after saving the file but before running `strfile`:

```shell
grep -v "^%" jackhandy | sort | sed -e 's/$/\n%/g' > jackhandy
```

I recommend you make a backup beforehand, especially in the event the GNU-specific `\n` in the `sed` substition doesn't work on your distro.

```
Your Deep Thought for this session:
 ________________________________________
/ If you ever reach total enlightenment  \
| while you're drinking a beer, I bet it |
\ makes beer shoot out your nose.        /
 ----------------------------------------
        \   ^__^
         \  (xx)\_______
            (__)\       )\/\
             U  ||----w |
                ||     ||
```