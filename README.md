# stowman

```bash
   _==_ _
 _,(",)|_|
  \/. \-|   stowman
__( :  )|_  Manage your dotfiles easily.

```

## Installation

Download the script as `stowman`:

```bash
curl -L https://raw.githubusercontent.com/filippo-orru/stowman/refs/heads/main/stowman.sh > ~/.local/bin/stowman
chmod +x ~/.local/bin/stowman
```

Or clone the repo:

```bash
git clone https://github.com/ad-on-is/stowman
cd stowman
chmod +x ./stowman.sh
ln -s "$PWD/stowman.sh" ~/.local/bin/stowman
```

## Usage

### Environment variables

- `STOWMAN_DOTDIR`: The directory where stowman will store your dotfiles (default: `~/.dotfiles`).
- `STOWMAN_HOMEDIR`: The directory where stowman will stow your dotfiles (default: `~/`).

### On your current machine

- Create a GitHub repository.
- Run `stowman init <repo>`
- Add files or folders to stowman using `stowman add <file/folder> <package>`
- Push changes using `stowman push`

### On another machine

- Run `stowman init <repo>`
- Reload the configuration by using `stowman reload <package|all>`

### Adding files or folders

- Run `stowman add ~/.config/nvim editors` to add `~/.config/nvim` to the `editors` package.
- Run `stowman add . cli` to add the current directory to the `cli` package.

### Syncing changes

- Run `stowman push` to update the repository.
- Run `stowman pull` followed by `stowman reload <package|all>` to pull and apply the latest changes.

### List stowed files and folders

- Run `stowman list` to list all stowed files and folders.
