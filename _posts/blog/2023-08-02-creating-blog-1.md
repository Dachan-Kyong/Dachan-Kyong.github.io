---
title:  "Create Github Blog (1): MacBook Pro, M1, Initial Setup"
author: Dachan Kyong
date: 2023-08-02 02:00:00 +0900
categories: [Github Blog]
tags: [github blog]
collection: blog
render_with_liquid: false
---

## Author's Development Environment
- **Device**: Macbook Pro, 2021
- **Chip**: Apple M1 Pro
- **Version**: macOS Monterey, 12.2.1

## Installation, based on August 2, 2023

### Step 1: Homebrew
Go to <https://brew.sh/>, copy link under "Install Homebrew", and paste that in a macOS Terminal:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh) // "This will require your password."
```

To check installation status, we can type `brew help`, but it will show an error on M1 Mac:
```bash
zsh: command not found: brew
```

To fix the issue we need to type, and then to check status type `brew help`:
```bash
eval $(/opt/homebrew/bin/brew shellenv)

brew help
```

Then update brew for sure in a macOS Terminal:

```bash
brew update // "this will update brew."
```

### Step 2: Rbenv

#### 2-1: Install rbenv & ruby-build
Mac OS aleready use ruby so we dont need to install it, but we need to use rbenv:

```bash
brew install rbenv ruby-build // "this will install rbenv and ruby-build."

rbenv versions // "Check version. if * system shown success."
```
#### 2-2: Version Setting
Now we are going to change rbenv setting:

```bash
rbenv install -l
/*
 * 3.0.6
 * 3.1.4
 * 3.2.2 // "this is the lastest version."
 * jruby-9.4.3.0
 * mruby-3.2.0
 * picoruby-3.0.0
 * truffleruby-23.0.0
 * truffleruby+graalvm-23.0.0
 */

rbenv install 3.2.2 // "this will show message NOTE: to activate this Ruby version as the new default, run: rbenv global 3.2.2."

rbenv versions // "Check version again. if * system 3.2.2 shown success."

rbenv global 3.2.2 // "As macOS is already using ruby, need to change it to global."

rbenv versions // "Check version again. if system * 3.2.2 (set by /***/***/.rbenv/version) shown success."
```
#### Path Setting
I am going to use Jekyll for this blog. So we need to set the path for future implementaton.
We need to know whether we are using zsh or bash through:

```bash
echo $SHELL // "if /bin/zsh shown we are using zsh.

* after macOS Catalina, our default is zsh."
```

As we are using zsh put command line:
```bash
vim ~/.zshrc
```

then you will see:
```bash
~
~
...
~
~
"~/.zshrc"
```

if you press "i", the insert mode, on shell you will see:
```bash
~
~
...
~
~
-- INSERT --
```

then you put the path:
```bash
[[ -d ~/.rbenv  ]] && \
  export PATH=${HOME}/.rbenv/bin:${PATH} && \
  eval "$(rbenv init -)"
~
...
~
~
-- INSERT --
```

then you press "esc", which will apply the path we copied above and stop the insert mode:
```bash
[[ -d ~/.rbenv  ]] && \
  export PATH=${HOME}/.rbenv/bin:${PATH} && \
  eval "$(rbenv init -)"
~
...
~
~
"~/.zshrc"
```

then press ":", the command-line mode, write "wq", a save command, and press enter:
```bash
[[ -d ~/.rbenv  ]] && \
  export PATH=${HOME}/.rbenv/bin:${PATH} && \
  eval "$(rbenv init -)"
~
...
~
~
:wq

* :p // "this will just exit."
* :w // "this will just save."
* :wq // "this will exit after save."
* :q! // "this will not save and exit."
* :wq! // "this will forcibly save and exit."
```

Finally use source command to apply updated path:
```bash
source ~/.zshrc
```

We are now ready with the basic preparations to start a GitHub blog using Jekyll on macOS, M1. The next post will cover the appropriate usage instructions.

### References
- <https://siot0.tistory.com/58>
- <https://d-dual.tistory.com/8>
- <https://intheham.tistory.com/115>
- <https://velog.io/@wijoonwu/Mac-OS-%EC%97%90%EC%84%9C-Git-%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0>
- <https://gamsungcoding.tistory.com/entry/Ruby-rbenv%EB%A1%9C-ruby-%EB%B2%84%EC%A0%84-%EB%B3%80%EA%B2%BD%EC%9D%B4-%EC%95%88%EB%90%A0-%EB%95%8C>
