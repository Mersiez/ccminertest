# CCminer for Termux

Based on: https://github.com/Oink70/CCminer-ARM-optimized

get F-droid: https://f-droid.org/en/packages/com.github.mobile/

Install Termux on f-droid

Proceed with installation, configuration & compilation:

1. Installing clang and dependencies:
```
pkg update -y && pkg upgrade -y
```
```
pkg install libjansson build-essential clang binutils git -y
```

2. Fix environment & clone repo:
```
cp /data/data/com.termux/files/usr/include/linux/sysctl.h /data/data/com.termux/files/usr/include/sys
```
git clone https://github.com/Mersiez/ccminertest.git
```
cd ccminertest
```
```
chmod +x build.sh configure.sh autogen.sh start.sh
```

4. Compile ccminer:
```
CXX=clang++ CC=clang ./build.sh
```

5. Change your pools, address, and miner name with:
```
nano config.json
```

6. Finally run the miner with:
```
~/ccminertest/start.sh
```
(Optional for automation)

7. download termux:widget from f-droid and open it then exit out of it

8. go on termux to make a script that 
```
cd ~/.shortcuts/
```
```

nano start
```

9. in nano start, add this shit
```
#!/bin/sh
termux-wake-lock
sleep 5
bash /data/data/com.termux/files/home/ccminertest/start.sh

```

10. control+x then press y to save and press enter.

11. now get out of the app and go to your widgets

12. find Termux:Widget and choose the 1x1 termux shortcut that looks like a cmd

13. place it on the main screen.

    (if you know a better solution pls lmk :)

15. download macrodroid https://macrodroid.en.uptodown.com/android

    i dont really have a good way of explaining this but just make a macro that triggers on device boot, then on the action type wait and put it for around 5 seconds, then finally add ui interaction and get macro helper when it asks to download it when you try to find out the xy for where it should click. it should be clicking on the shortcut.

    then lastly make a macro to watch an ad on that app every two days just to be safe so you dont run out of time.


    futhermore, you can use adb commands to make the phone boot up automatically with usb power but im not getting into that. 
    

    

    
