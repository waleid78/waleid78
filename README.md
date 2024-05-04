@echo off
setlocal enableDelayedExpansion
echo '''''''''''''''''''''''''''''''''''''''' 
echo '''''''''''''''''''''''''''''''''''''''' 
echo " ______                               "
echo "|_   _ \                              "
echo "  | |_) |  _   __                     "
echo "  |  __'. [ \ [  ]                    "
echo " _| |__) | \ '/ /                     "
echo "|_______/[\_:  /_____  ____  ____     "
echo "|_   __ \ \__.'|_   _||_   ||   _|    "
echo "  | |__) |       | |    | |__| |      "
echo "  |  __ /    _   | |    |  __  |      "
echo " _| |  \ \_ | |__' |   _| |  | |_     "
echo "|____| |___|`.____.'  |____||____|    "
echo "  _____     ____     _____   ______   "
echo " / ___ `. .'    '.  / ___ `./ ____ `. "
echo "|_/___) ||  .--.  ||_/___) |`'  __) | "
echo " .'____.'| |    | | .'____.'_  |__ '. "
echo "/ /_____ |  `--'  |/ /_____| \____) | "
echo "|_______| '.____.' |_______|\______.' "
echo '''''''''''''''''''''''''''''''''''''''' 
echo ''''''''''''''''''''''''''''''''''''''''
echo starting the system ...
Start "" "index.html"
echo Start folder monitoring for any downloaded files ...  
echo If you would like to exit, press CTRL+c, then Y
echo ...

:loop
if exist "customers.txt" (
    del "customers.js" 2>NUL 
    ren "customers.txt"  "customers.js" 2>NUL
    del "customers *.txt" 2>NUL 
)
if exist "drivers.txt" (
    del "drivers.js" 2>NUL 
    ren "drivers.txt"  "drivers.js" 2>NUL
    del "drivers *.txt" 2>NUL 
)
if exist "orders.txt" (
    del "orders.js" 2>NUL 
    ren "orders.txt"  "orders.js" 2>NUL
    del "orders *.txt" 2>NUL 
)
if exist "quantities.txt" (
    del "quantities.js" 2>NUL 
    ren "quantities.txt"  "quantities.js" 2>NUL
    del "quantities *.txt" 2>NUL 
)

timeout /t 60 /nobreak > NUL
goto loop
pause
"D:\OneDrive - Aqaba Water Company\Desktop\نظام تتبع تنكات المياه\نظام تتبع تنكات المياه\index.html"
