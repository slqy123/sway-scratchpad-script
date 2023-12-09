# Intro
This is a simple script to show/hide specific window from sway scratchpad.

It works like:
```javacript
(binding key pressed) => {
    if (window not exists) {
        open the application;
        move to scratchpad;
        show from scratchpad;
    }
    else {
        show/hide the window;
    }
}
```

# Usage
```
git clone https://github.com/slqy123/sway-scratchpad-script.git
cd sway-scratchpad-script
chmod +x scratchpad
cp scratchpad scratchpad.toml ~/.config/sway
```
After that, modify `scratchpad.toml` and add the following command in you sway config file:
```
exec_always cd ~/.config/sway && ./scratchpad < scratchpad.toml
```
finally, reload your sway config.

# Else
This script is inspired by this [post](https://www.reddit.com/r/swaywm/comments/u3kw7y/hideshow_a_window/) 

BTW, I personally use `mod = 'ctrl+Mod1+Mod4+shift'`, and use [keyd](https://github.com/rvaiya/keyd) to map it with `$mod+a`. here is my keyd config file:
```conf
[main]
leftmeta = layer(leftmeta)

[leftmeta:M]
a = layer(modall)

[modall:C-M-A-S]
```
