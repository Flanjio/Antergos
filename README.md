# Antergos
Installation Nvidia Optimus, config, logiciel.

*** Installation Antergos sur Nvidia Optimus ***
1) https://antergos.com/wiki/fr/hardware/bumblebee-for-nvidia-optimus/
  Boot install antergos edit : modprobe.blacklist=nouveau

*** Configuration après installation ***
1) Pilote propiétaire Nvidia :
  https://wiki.archlinux.fr/NVIDIA#Pilote_propri.C3.A9taire
  Note : Si vous utilisez le noyau linux-lts, n'oubliez pas d'installer la version lts de votre pilote nvidia: nvidia-lts, etc.. 

2) Tearing :
  http://duncanlock.net/blog/2013/06/07/how-to-switch-to-compton-for-beautiful-tear-free-compositing-in-xfce/

*** Mise à jour et trie mirroirs ***
  https://wiki.archlinux.fr/Reflector
  1) pacman -S reflector
  
  2) Créez une sauvegarde de /etc/pacman.d/mirrorlist avant de continuer :
  cp -vf /etc/pacman.d/mirrorlist /etc/pacman.d/mirrorlist.backup
  
  3) Cette commande filtre les 5 miroirs qui ont été mis à jour tout récemment, les trie par vitesse puis écrase /etc/pacman.d/mirrorlist avec ces nouveaux miroirs :
  reflector --verbose -l 5 --sort rate --save /etc/pacman.d/mirrorlist
  
*** Theme ***
XFCE4
Theme: Arc-Dark
Icons : Papirus-Dark
Font: Open Sans Light 11
