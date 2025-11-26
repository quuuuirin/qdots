# Dotfiles install

## Required packages:

**Pacman**

    - hyprland 
    - wayland 
    - xorg-xwayland 
    - mesa 
    - libinput 
    - libdrm 
    - libxkbcommon 
    - wayland-protocols 
    - zsh 
    - git 
    - swww 
    - waybar 
    - rofi 
    - networkmanager
    - matugen
    - wlogout
    - cava
    - yay
    - nautilus
    - pamixer
    - brightnessctl
    - swaync-client
    - obsidian

**Yay**

    - unimatrix
    - peaclock

**Git**

    - https://github.com/pipeseroni/pipes.sh

## Delete old config

    rm -rf ~/.config


## Activate new config

    sudo cp -r ~/arch-hyprland/.config ~/
    sudo cp -r ~/arch-hyprland/wallpapers ./
    sudo cp ~/arch-hyprland/.zshrc ./


## Reboot

    sudo reboot

## Fix Bugs and Configure

- Comment out Line 7 in `~/.config/hypr/configs/Useranimations.conf`: `bezier = been2, 0,.94,.5,.99`
- Edit `~/.config/hypr/configs/input.conf`
    - Set KB-Layout to CH
    - Uncomment whole section `gestures {}`
- Edit `hyprland.conf`
    - Set monitor settings to: `monitor=,preferred,auto,1.3333334`
 
- Install oh-my-zsh!
  
        sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

- Install the already activated zsh-Plugins: 

        git clone https://github.com/zsh-users/zsh-autosuggestions ~/.oh-my-zsh/custom/plugins/zsh-autosuggestions
        git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ~/.oh-my-zsh/custom/plugins/zsh-syntax-highlighting

- Make all scripts executable:
        
        sudo chmod +x ~/.config/hypr/scripts/*

- Copy `wallpapers`-Folder into `~/Pictures/wallpapers`


## Fix .config Ownership

If Waybar or swww dont work correctly, try: `sudo chown -R $USER:$USER ~/.config`











