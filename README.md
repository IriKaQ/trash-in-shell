# trash-in-shell
This is a shell script tools for trash in terminal.

It provides an extra layer of protection for console deletions.

## features
1. Delete and restore files
2. Clear trash files
3. Delete and restore directories
4. Support wildcards *
   - Wildcard preposition
   - Willcard post
   - Wildcard middle
5. Show trash
6. Restore follow files when deleting
7. Restore follow directories when deleting
8. Support relative path for delete
9. Support relative path for restore

## not implements

## usage
The tool provide commands: `rm`, `rl`, `ur` and `cr`.

- `rm`: the command alias system `rm` program,
and it only accepts files or directories to be deleted
without parameters like the system `rm`.
- `rl`: list deleted files and directories.
- `ur`: restore deleted files or directories to original location,
and the parameters like `rm`.
- `cr`: clear the trash.

## install
There are two ways to install the tool.

1. Auto installation
2. Manual installation

#### Auto installation
Run the `install.sh` script to auto install.

#### Manual installation
Copy the file `trash` to your preferred location and name as `.trash_script`,
such as you home directory,
and then add follow shell code to your `~/.bashrc` or `~/.profile`.
**Note**: `~/.bashrc` __FIRST__ and then `~/.profile`.

``` shell
# include ~/.trash_script if it exists
if [ -f "$HOME/.trash_script" ]; then
    . "$HOME/.trash_script"
fi
```

## uninstall
1. Delete file `~/.trash_script`
2. Delete text as above code from your `~/.bashrc` or `~/.profile`

## NOTE
1. If you want to use wildcard to restore files or directories,
the parameter __MUST__ wrapped in quotation marks (" " OR ' ').
