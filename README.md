# Dotdock #

The easy way to manage system configuration and dotfiles. Version controlled dotfiles without symlink litter.

(c)2017 Stephen Parker (https://withaspark.com). All rights reserved. See [LICENSE](LICENSE).

## INSTALL: ##
1. Install Dotdock to a bin directory (`~/bin`, `/usr/local/bin`, etc.).
   ```sh
   git clone --depth=1 https://github.com/withaspark/dotdock.git $HOME/.dotdock
   sudo cp $HOME/.dotdock/dotdock /usr/local/bin/dotdock; sudo chmod ugo+rx /usr/local/bin/dotdock
   ```
2. Create a remote repository to backup or publish configuration files to.
3. Configure Dotdock.
   ```sh
   cp $HOME/.dotdock/.env.example $HOME/.dotdock/.env
   ```
   * Set `REPO_URL` to the URL of the new remote repository created above.
4. Initialize Dotdock file repository.
   ```sh
   dotdock init
   ```

## USAGE: ##
    dotdock add FILE
    dotdock diff [FILE]
    dotdock init
    dotdock list
    dotdock publish
    dotdock pull [FILE]
    dotdock rm FILE
    dotdock save [FILE]
    dotdock status

## COMMANDS: ##
`a|add FILE`<br>
Adds a file to the managed configuration files.

`d|diff [FILE]`<br>
Shows the differences between a managed configuration file and the current state of the file.

`i|init`<br>
Inits the managed configuration file repository.

`l|list`<br>
Lists the managed configuration files.

`publish`<br>
Publishes all local managed configuration files to the repository.

`pull [FILE]`<br>
Updates all local managed configuration files with the versions being tracked.

`rm|remove|del|delete FILE`<br>
Removes a file from the managed configuration files.

`save [FILE]`<br>
Saves the current state of a managed configuration file to the file repository.

`s|status`<br>
Shows the change status of the managed configuration file repository.

## OPTIONS: ##
`-v|--version`<br>
Gets the current version of Dotdock.

`-h|--help`<br>
Shows help and usage.
