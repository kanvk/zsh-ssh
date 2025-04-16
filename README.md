# zsh-ssh

Better host completion for ssh in Zsh.

Forked from [zsh-ssh](https://github.com/sunlei/zsh-ssh). I've made some minor improvements to address issues I've had with the plugin.

[![asciicast](https://asciinema.org/a/381405.svg)](https://asciinema.org/a/381405)

- [zsh-ssh](#zsh-ssh)
  - [Installation](#installation)
    - [Zinit](#zinit)
    - [Antigen](#antigen)
    - [Oh My Zsh](#oh-my-zsh)
    - [Sheldon](#sheldon)
    - [Manual (Git Clone)](#manual-git-clone)
  - [Usage](#usage)
    - [SSH Config Example](#ssh-config-example)

## Installation

Make sure you have [fzf](https://github.com/junegunn/fzf) installed.

### Zinit

```shell
zinit light kanvk/zsh-ssh
```

### Antigen

```shell
antigen bundle kanvk/zsh-ssh
```

### Oh My Zsh

1. Clone this repository into `$ZSH_CUSTOM/plugins` (by default `~/.oh-my-zsh/custom/plugins`)

   ```shell
   git clone https://github.com/kanvk/zsh-ssh ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-ssh
   ```

2. Add the plugin to the list of plugins for Oh My Zsh to load (inside `~/.zshrc`):

   ```shell
   plugins=(zsh-ssh $plugins)
   ```

3. Start a new terminal session.

### Sheldon

1. Add this config to `~/.config/sheldon/plugins.toml`

   ```toml
   [plugins.zsh-ssh]
   github = 'kanvk/zsh-ssh'
   ```

2. Run `sheldon lock` to install the plugin.

3. Start a new terminal session.

### Manual (Git Clone)

1. Clone this repository somewhere on your machine. For example: `~/.zsh/zsh-ssh`.

   ```shell
   git clone https://github.com/kanvk/zsh-ssh ~/.zsh/zsh-ssh
   ```

2. Add the following to your `.zshrc`:

   ```shell
   source ~/.zsh/zsh-ssh/zsh-ssh.zsh
   ```

3. Start a new terminal session.

## Usage

Just press <kbd>Tab</kbd> after `ssh` command as usual.

### SSH Config Example

You can use `#_Desc` to set description.

~/.ssh/config

```text
Host Bastion-Host
    Hostname 1.1.1.1
    User kanvk

Host Development-Host
    Hostname 2.2.2.2
    IdentityFile ~/.ssh/development-host
    #_Desc For Development
```
