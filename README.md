# Dotfiles

Configuration files to automate the setup of my macos development environment.

The installation script is a "rolling" setup, which means you can run it multiple times without worrying to screw things up, so if you want to change the setup you can update this repo and run the script again.

## Installation

Clone the repository:
```sh
git clone git@github.com:b1n01/dotfiles.git ~/.dotfiles 
```

And run the installation script:
```sh
sh ~/.dotfiles/install.sh
```

## Dependencies

The installation script will install and setup:

- [Homebrew](https://github.com/Homebrew/brew)
- [Oh-my-zsh](https://github.com/ohmyzsh/ohmyzsh)
    - [Powerlevel10k](https://github.com/romkatv/powerlevel10k) theme
    - [Autosuggestion](https://github.com/zsh-users/zsh-autosuggestions) plugin
- [Nvim](https://github.com/neovim/neovim)
    - [Packer](https://github.com/wbthomason/packer.nvim)
	- [Telescope](https://github.com/nvim-telescope/telescope.nvim)
	- [Treesitter](https://github.com/nvim-treesitter/nvim-treesitter)
	- [Nvim-tree](https://github.com/kyazdani42/nvim-tree.lua)
    - [Github theme](https://github.com/projekt0n/github-nvim-theme)
- [Alactritty](https://github.com/alacritty/alacritty)
    - [Github theme](https://github.com/projekt0n/github-nvim-theme/tree/main/terminal/alacritty)

Optional dependencies:

- [Amethyst](https://github.com/ianyh/Amethyst)
- Google Chrome
- Visual Studio Code
- Docker desktop
- PHPStorm
- Slack

### Telescope

The following Telescope key binds are available (defined in `nvim/telescope.lua`):

```
\ff # Find files
\fg # Live grep
\fb # Show buffers
```

### Treesitter

To install a new language run the Nvim command:

```
:TSInstall language # install a language
:TSInstallInfo      # list of all available languages
```

To ensure a language is always installed add the language to the `ensure_installed` array in `nvim/treesitter.lua` 

### Nvim-tree

The following Nvim-tree key binds are available (defined in `nvim/tree.lua`):
```
\e # Toggle tree buffer
```


## Alias and function documentation

The `list` function prints out all available aliases and functions, to make this work there a special syntax:
```
#@doc name: Desctiption
```

## Caveat

- The first time alacritty is opened it must be done with `control + click` and then `Open`
- The setup is on early development and it has been created on MacOS 12.4 Monterrey, could not work on other system. Please backup your configuration files before running any script
