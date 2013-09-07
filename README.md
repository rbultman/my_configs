A place to stick common config files for use across multiple machines.

#### Background
Configuration files are stored in your home directory in .config in a series of directories,
one per configuration file.  If you want to share these configuration files across multiple
machines, you can use github to do so.

#### From the start

1. Create a github repo in order to store your config files.
2. Create a directory in which to store the files.
    mkdir ~/.my_configs
3. Change to the directory.
    cd ~/.my_configs
4. Initialize git
    git init
5. Create a README file and edit it. Put whatever notes you want in it.
    touch README.md 
    vi README.md
6. Add the README to git.
    git add README.md
7. Add a config file that you want to keep on github. This will copy the directory tree
associated with the config file.
    cp -R ~/.config/someConfigDir .
8. Add the config file to git
    git add someConfigDir
9. Remove the original config file and add the sym link to the new config location.
    rm -rf ~/.config/someConfigDir
    ln -s ~/.my_configs/someConfigDir ~/.config/someConfigDir
10. Commit everything
    git commit -m "Commit message"
11. Push to your repo
    git push -u origin master

# Create jj
To use:
1) Create a directory such as ~/.my_configs
2) 

