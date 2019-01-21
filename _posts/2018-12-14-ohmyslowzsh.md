---
layout: post
title: "Oh-my-SLOW-zsh: my transition back to bash"
date: 2018-12-14
categories: [short-post, bash, ohmyzsh]
image: /assets/images/2018/12/turbo.jpg
caption: "Turbo, 2013"
---

> **Disclaimer** This is not like my usual posts, and it's small in comparison. I'm not a "shell" power user, I'm a pretty dumb user compared to people who can do magic with stuff like awesome `awk` or `sed`. I also don't know a lot about `ohmyzsh` inner-workings, I just used some of its features. I'm writing this first and foremost as a guide for "future me" if I ever need to configure this again on another computer.

Recently I started noticing `ohmyzsh` functioning slowly for my daily usage, even on a modern Macbook Pro:

- New session bootup time - taking a lot of seconds every time I opened a new terminal session;
- Irritating latency between commands: Shell not being right away available to write after any command finished running - taking always 2-3 seconds more sometimes after I issue something as simple as an `echo hello` to allow me to write another command;

I tried a couple of workaround/fixes for this slowness, for example trying to not boot stuff like `nvm` whenever I start a new session, but it didn't do the trick for the slowness between writing commands. I definitely did NOT do any sort of in-deep study on the latency of the commands, this is, by far, not one of Dan Luu's awesome [latency studies](https://danluu.com/term-latency/).

After almost 2-3 years of using `ohmyzsh` I decided to try and switch back to plain bash with some minor workarounds, and see if I can get the "instant response" feeling of older days (that for some unknown reason seems lost).

Here are the steps I took to set up an environment where I'd be able to use `bash` with some comfort:

### 1) Getting free from zsh and the "hip and cool framework to configure it"

I [uninstalled ohmyzsh](https://github.com/robbyrussell/oh-my-zsh/#uninstalling-oh-my-zsh), and switched my default shell to bash:

```
chsh -s /bin/bash
```

### 2) Upgrading Mac's bash version from 3.2 to 4

Basically, I needed this for the `autocd` feature. Originally found in <https://clubmate.fi/upgrade-to-bash-4-in-mac-os-x/>:

```
brew update && brew install bash
$BASH_VERSION
sudo bash -c 'echo /usr/local/bin/bash >> /etc/shells'
chsh -s /usr/local/bin/bash
```

### 3) Setup bash autocd feature and list shortcuts

I know I'd miss the feature of not having to write down `cd` to switch between dirs, in `bash 4` this did the trick for me:

```
shopt -s autocd
```

Also, for comfort, added a few `ls` shortcuts to my `.bashrc` file:

```
alias ls='ls -G'
alias l='ls -lah'
```

### 4) Setup git aliases similar to the ones of the ohmyzsh git plugin

I'm using [oh-my-git-aliases.sh](https://github.com/filfreire/oh-my-git-aliases) (fork from [mjkonarski](https://github.com/mjkonarski/oh-my-git-aliases)), I added something similar to this to my `.bashrc`:

```
source "$HOME/.some_scripts_folder/oh-my-git-aliases.sh"
```

### 5) Show branch name in git versioned folders

Not sure how to do this for now, writing down `git branch` will have to do it in the meantime.

## Final result and remarks

My endeavors in the console world feel "instant"-like again and don't irritate me. I didn't go very in deep to investigate the performance issues with `ohmyzsh`, maybe sometime in the future, I'll dedicate a bit of time solely for that.

I'm not sure I'll ever get back to using `ohmyzsh`. To be fair with `ohmyzsh`, I'll say this again, I didn't invest a ton of time researching on more ways of trying to optimize it, at one point the slowness was very irritating, so I just switched back to something that, for now works perfectly for me, which is plain old `bash` with some tweaks.
