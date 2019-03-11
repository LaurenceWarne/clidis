# clidis
A command line display manager to start your desktop more intractive!

![clidis preview](https://raw.githubusercontent.com/virtualdemon/clidis/master/screenshot/screenshot_v-2.0.png)

![RepoSize](https://img.shields.io/github/repo-size/hamidrezakp/clidis.svg) ![Contributors](https://img.shields.io/github/contributors/hamidrezakp/clidis.svg?style=flat-square)
    
## automatic installation

1. Download the script with `curl` or `wget` : 
	
    `wget https://raw.githubusercontent.com/hamidrezakp/clidis/master/clidis -O ~/.clidis`

	`curl https://raw.githubusercontent.com/hamidrezakp/clidis/master/clidis -o ~/.clidis`
	        
2. Change script permission : 

	`chmod +x ./clidis`

3. Run it with `-i` or `--install` switch : 

    `./clidis -i`

## remove automatically

Just run it with `-u` or `--uninstall` switch : `./clidis -u`


## test  mode

After downloading the script you can just use `-t` or `--test-mode` to see what it's look like! : `./clidis -t`

## configuration

The clidis configuartion is in **~/.config/clidis/config** you can tweak clidis alittle with defined variables! please don't mess with `systemDefaultDisplayManager` and `lastUserChoice` variable!

You can enable or disable showing system status under the clidis logo and tweak them. 0 is for disable and 1 is for enable.

## manual installation

1. Download the script with `curl` or `wget` into your home directory : 
	
    `wget https://raw.githubusercontent.com/virtualdemon/clidis/master/clidis -O ~/.clidis`

	`curl https://raw.githubusercontent.com/virtualdemon/clidis/master/clidis -o clidis`
	        
2. Change script permission : 

	`chmod +x ~/.clidis`
    
3. Disable your current display manager : 

    `sudo systemctl disable display-manager.service`

4. Append the following line into your login shell profile (`zsh` -> **~/.zprofile** | `fish` -> **~/.config/fish/config.fish** | `bash` -> **~/.bash_profile**) : 
    
    `exec bash $HOME/.clidis`
     
     For fish shell just run this command : 
     
     `echo -e "if status --is-login\n\texec bash $HOME/.clidis\nend" >> $HOME/.config/fish/config.fish`
     
    If you don't know what's your login shell, just run this command : 
    
    `echo $SHELL`
	
5. Reboot your system : `reboot`

## manually remove

1. Remove $HOME/.clidis : `rm ~/.clidis`

2. Remove clidis line from your login shell profile : `sed '/clidis/d' /path/to/shell_profile`

3. Enable your display manager : `sudo systemctl enable YourDisplayManagerService`

4. Reboot the system : `reboot`
    
### TODO
   - [x] Adding squares to select options
   - [x] Adding vim key's for moving around options
   - [x] Adding config file
   - [ ] Adding power options ( reboot, shutdown , ... )
   - [ ] Adding Sabooh (@mostafaAsadi) option to login page
   - [ ] Adding systemd-analyze to login page
    
### MORE

>  special thanks to :
    MisterH
    virtualdemon
    
Made with :heart: for cli users!

