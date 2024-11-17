# Using this versioned dotfiles stuff

Ideally you will have your dotfiles at `~/` so create a directory where all the stow packages will be stored. Lets say the new dir is called `stow`, bc I don't have imagination. 
This repo can be understood as a stow package, so, it should be cloned inside the `~/stow/` dir, be sure it is cloned as a directory containing the dot-files.
Stow rely on how the directories are mirroring the scheme used in the actual file system. Read more in the Stow page.

# Create the symlinks

The following command should be run at `~/stow/dotfiles` directory:

```bash
stow --dotfiles config
```

# Sync new dotfiles

New files in the dotfiles dir managed by stow were added, so those files are not symlinks.
This command should be used carefully.
Be sure the dotfiles you want to adopt are placed at the stow package. Optionally use the `-n` and `--verbose=3` to se how the changes will be performed.

```bash
stow --adopt --dotfiles
```

In case of having to remove symlinks, probably is better do it using stow. If not, be sure the symlinks are being removed and not the actual files.

