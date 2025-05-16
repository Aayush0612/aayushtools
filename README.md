# aayushtools
tools i made for my arch linux install which other devs can also use to make their lives easier

1. keyboard-backlight: Control your keyboard brightness
  Install brightnessctl using sudo pacman -S brightnessctl
  List available devices: brightnessctl -l
  Identify your keyboard backlight device
  Save the script as ~/bin/keyboard-backlight
  Edit the device name from 'platform::kbd_backlight' to whichever you have
  Edit the values if you want to as yours could differ

  Now, make it executable using
  mkdir -p ~/bin
  chmod +x ~/bin/keyboard-backlight

  Now, create symlinks
  ln -s ~/bin/keyboard-backlight ~/bin/keyboardmax
  ln -s ~/bin/keyboard-backlight ~/bin/keyboardmin
  ln -s ~/bin/keyboard-backlight ~/bin/keyboardmed

  Add your bin directory to PATH (if not already there):
  echo 'export PATH="$HOME/bin:$PATH"' >> ~/.bashrc
  source ~/.bashrc

  PS: I'm using bash, if you're using something else, like ksh/zsh/fish edit it.

  use keyboardmax to max out the brightness
  use keyboardmed to set it to medium
  use keyboardmin to turn it off

  enjoy, more tools coming soon!
