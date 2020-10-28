# openbox-installing-configuraing
This is step by step tutorial on  installing openbox window manager and configuring openbox in Arch Linux
# Step by step Commands used in Installing and configuring openbox in Arch Linux
#
# Installing xorg X11 server type the following command then press enter for the default:-
#-----------------------------------------------------------------------------------------
# pacman -S xorg-server
#
# installing the nessesery following packages:-
# ----------------------------------------------
# installing sudo ,lightdm(log-in-manager),lightdm-gtk-greeter,openbox(window manager),obconf(configure         # openbox),obmenu(configure the right click menu),nitrogen(wallpaper manager),featherpad(text editor) arandr
# (screen resolution manger),and geany           
# tint2(panel),xterm(terminal),termite(terminal),and firefox(web browser).
#
# Type the following command without # to install all of the previous packages:-
# -------------------------------------------------------------------------------
# pacman -S sudo lightdm lightdm-gtk-greeter openbox obconf nitrogen tint2 xterm termite featherpad arandr
# firefox obmenu
#  Note:- you must be the root user throughout this step by step tutorial
#
# Enable the log-in manager lightdm at boot type the following command:-
#----------------------------------------------------------------------
# systemctl enable lightdm.service
#
# To give the standard user the sudo Privileges and making nano the default text editor in the terminal we type # The following command without #:-
# -----------------------------------------------------------------------------------------
# EDITOR=nano visudo
# Then uncomment the TWO following lines in this visudo file:- 
# % wheel ALL=(ALL)ALL
# uncomment to allow memeber of group wheel to execute any command:-
# % sudo ALL=(ALL)ALL
# uncomment mean deleting the # then go to the next step
# Press ctrl then press letter o then press enter to save then press ctrl then press x to exit.
#
# Installing the gnome backgrounds type the following command without # in the terminal:-
#-----------------------------------------------------------------------------------------
# pacman -S gnome-backgrounds
# Open nitrogen by typing nitrogen in the xterm terminal then hit enter then click preferances then
# click filesystem folder then click user folder then backgrounds folder then gnome folder then click select
# then click ok then choose any wallpaper click apply make sure you select the on scale option to get full
# screen.
#
# Creating Autostart-file to keep and preserve wallpaper and tint2-panel after log-out and log in of openbox
# ----------------------------------------------------------------------------------------------------------
# Open any file manager open home folder click view tap click show hidden files then you will see.config folder
# creat a folder name openbox inside the.config folder then creat a blank text file name autostart using any
# text example featherpad
# editor inside the openbox folder.
# Type inside this blank autostart file the following two lines without the #
# tint2 &
# nitrogen --restore &
# then click save then log out and then log in you will notice the wallpaper and the panel did not disappear
# the autostart configration will preserve your background wallpaper and the panel(tint2).
#
# Installing the menumaker type the following command in the terminal (remmber which terminal you used):-
# ---------------------------------------------------------------------------------------------------------
# sudo pacman -S menumaker
# To run and enable the mmaker openbox type the following command and type the name of terminal you used in the
# previous command of installing menumaker NOTE we type the name of the terminal xterm:-
# mmaker openbox -f -t xterm
# Note we type xterm because we used the xterm terminal when we installed menumaker.
# Then right click then click reconfigure openbox watch now you have all of the application in the right click    # menu.
#
# For other distro of linux other than Arch linux go to the following link to get menumaker:-
# https://sourceforg.net/projects/menumaker/
#
# For virtualbox machine to get full screen of your wallpaper if your wallpaper is not going for full screen
# then install the guest edition for virtualbox Type the following command then reboot the virtualbox machine
# sudo pacman -S virtualbox-guest-utils
# sudo reboot
#
# Configuring autostart file in the openbox folder to restore the wallpaper after loging out and in of openbox
# ------------------------------------------------------------------------------------------------------------
# I have a duplicate openbox folder with this tutorial to get to your openbox folder in your system go 
# your home folder then to the .config folder make sure you click show hidden files under the view tap then you # will see the openbox folder open it copy every thing in openbox folder of this tutorial and pate it in your
# openbox folder that in your system.
# click reconfigure openbox from the right click menu(obmenu).
# Editing the right click menu first make sure that obmenu is installed in your system,if not installed then 
# typing the following command in your terminal:-
# sudo pacman - S obmenu
# then Type obmenu in the terminal then add the following items for the right click menu by click on internet 
# for example then click on add items then type in the command box firefox and the in the name box type Firefox # to find out the right command that you need to type command box for vivaldi browser for example click on the # search application finder icon open the application finder(xfce4) then click internet then hover your mouse 
# over vivaldi browser then you will see the command that you need to enter in obmenu-command box in this case # the command is vivaldi-stable
# 
# Done -Thank you!!- This Step by step tutorial Document Written by AREF AHMED E-MAIL sabata4000@gmail.com
