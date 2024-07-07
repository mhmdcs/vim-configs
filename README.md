# My personal vim configurations

## Introduction

This repo contains my personal neovim configurations, so that if I switch around between different machines (at home, work, etc) I just clone this repo, and in case I screw up my configs somehow, I can always rollback through my git commit history :)

## Installation

### Install Neovim

Install either the latest
['stable'](https://github.com/neovim/neovim/releases/tag/stable) or latest
['nightly'](https://github.com/neovim/neovim/releases/tag/nightly) of Neovim.

### Install External Dependencies

External Requirements:
- Basic utils: `git`, `make`, `unzip`, C Compiler (`gcc`)
- [ripgrep](https://github.com/BurntSushi/ripgrep#installation)
- Clipboard tool (xclip/xsel/win32yank or other depending on platform)
- A [Nerd Font](https://www.nerdfonts.com/): optional, provides various icons
  - if `vim.g.have_nerd_font` in `init.lua` is set to true
- Language Setup:
  - If want to write Typescript, you need `npm`
  - If want to write Golang, you will need `go`
  - etc.

### Install

Neovim's configurations are located under the following paths, depending on the OS:

| OS | PATH |
| :- | :--- |
| Linux, MacOS | `$XDG_CONFIG_HOME/nvim`, `~/.config/nvim` |
| Windows (cmd)| `%userprofile%\AppData\Local\nvim\` |
| Windows (powershell)| `$env:USERPROFILE\AppData\Local\nvim\` |

#### Clone the repo

If on Mac:
```sh
git clone https://github.com/mhmdcs/vim-configs.git "${XDG_CONFIG_HOME:-$HOME/.config}"/nvim
```

If on Windows:
`cmd.exe`:

```
git clone https://github.com/mhmdcs/vim-configs.git %userprofile%\AppData\Local\nvim\
```

`powershell.exe`

```
git clone https://github.com/nvim-lua/kickstart.nvim.git $env:USERPROFILE\AppData\Local\nvim\
```

### Post Installation

Start Neovim

```sh
nvim
```

Lazy plugin manager (lazy.nvim) will install all the plugins automatically. Use `:Lazy` to view
current plugin status. Hit `q` to close the window.

### FAQ

Will update with notes if needed.

### Install External Dependencies (Prerequisites)

Below are OS specific install instructions for Neovim and dependencies.

After installing all the dependencies (prerequisites) on the new machine, then clone this repo to set up the configs.

#### Windows Installation

<details><summary>WSL (Windows Subsystem for Linux)</summary>

```
wsl --install
wsl
sudo add-apt-repository ppa:neovim-ppa/unstable -y
sudo apt update
sudo apt install make gcc ripgrep unzip git xclip neovim
```
</details>

#### Linux Install
<details><summary>Ubuntu Install Steps</summary>

```
sudo add-apt-repository ppa:neovim-ppa/unstable -y
sudo apt update
sudo apt install make gcc ripgrep unzip git xclip neovim
```
</details>
