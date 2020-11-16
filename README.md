# KPrepublic MKB87

# Specs

1. Full RGB LEDS(support kinds of light effects)
2. Full Switch Hot swappable sockets(can support both 3pin and 5pin switches)
3. Dual Mode(cable Mode+Bluetooth 5.0 Mode)
4. Type C(USB detachable design)
5. NKRO
6. Setting Memory Core

## How to use Bluetooth mode

1. Turn on battery button at bottom of case
2. Fn+Tab change to Bluetooth mode
3. Fn+Q/W/E to choose 1 device
4. Press Fn+P for 5 sec, make sure MKB87 is in bluetooth pairing mode
5. Open your pc or mobile device Bluetooth function, then search keyboard and connect it.

**Pls pay attention: when you connect with PC through cable, pls make sure you turn off the battery button and press Fn+tab to change the MKB87 to Cable mode, otherwise the keyboard wont work.**

**The green indicator light below the space button is on, indicating that the battery is charging. When the power is 100%, the green indicator will automatically turn off**

## **Keyboard Combinations**

* Fn+Arrow Keys----Adjust brightness and RGB effect speed 
* Fn+Ins---RGB led on/off
* Fn+PgUp---Lighting effect cycle(RGB color)
* Fn+PgDn---Lighting effect cycle(single color)
* Fn+Tab---Cable Mode/Bluetooth Mode change
* Fn+P for 5 sec---Bluetooth pairing mode
* Fn+Q/W/E---You can change between 3 different bluetooth device
* Fn+Win---Lock/Unlock Win
* Fn+Spacebar for 3 sec----Reset default setting
* Fn+S---MAC OS Mode
* Fn+A---Win Mode

# FAQ

## Function keys only register as Media Keys when using Linux

[...] Change the fnmode variable on your system from the boolean 1 to 0. You should be able to do this by piping an echo 0 command to tee on the file itself:

```
echo 0 | sudo tee /sys/module/hid_apple/parameters/fnmode
```

If that doesn't work, remember to set it back to 1 for consistency's sake:

```
echo 1 | sudo tee /sys/module/hid_apple/parameters/fnmode
```

Source: https://www.reddit.com/r/MechanicalKeyboards/comments/d5io49/keychron_k2_f_keys_dont_work_w_linux_help/

Permanent:

```
echo "options hid_apple fnmode=0" | sudo tee /etc/modprobe.d/hid_apple.conf
sudo update-initramfs -u -k all
```

Optional afterwards: `reboot`

Source: https://unix.stackexchange.com/questions/121395/on-an-apple-keyboard-under-linux-how-do-i-make-the-function-keys-work-without-t