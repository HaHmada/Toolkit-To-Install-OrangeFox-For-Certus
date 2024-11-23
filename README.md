**Toolkit FlashTWRP For Redmi 6/6A** 

This Toolkit Makes It Easy For You To Install TWRP On Redmi 6/6A With Your Computer

**Warning!!!** This Toolkit Only For Windows XP Or New Version Of Windows 

**You Can Create This Toolkit (Only For Windows 7 or New Version)**

Tools

- [Git For Windows](https://objects.githubusercontent.com/github-production-release-asset-2e65be/23216272/bfdf16e8-03fa-4c64-a1d3-a789f642fcc4?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=releaseassetproduction%2F20241116%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20241116T103538Z&X-Amz-Expires=300&X-Amz-Signature=a7a9c536d49566e7816a0f575bca08b26531e733d9afd5a8b70f0813e5379f6b&X-Amz-SignedHeaders=host&response-content-disposition=attachment%3B%20filename%3DGit-2.47.0.2-64-bit.exe&response-content-type=application%2Foctet-stream "Git")

- [OrangeFox For Certus](https://dl.orangefox.download/62408c446a44bc73841965cf "OrangeFox")

- [Notepad++](https://objects.githubusercontent.com/github-production-release-asset-2e65be/33014811/bef2b9f5-438d-4a80-b556-86ae83d9273c?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=releaseassetproduction%2F20241116%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20241116T104207Z&X-Amz-Expires=300&X-Amz-Signature=069c39f35581277ecf70c30d0e5b4cdf64cabcefd6a0dc847fb6d23edf26dc75&X-Amz-SignedHeaders=host&response-content-disposition=attachment%3B%20filename%3Dnpp.8.7.1.Installer.x64.exe&response-content-type=application%2Foctet-stream "Notepad++")

**Note**: Extract OrangeFox Files Before Starting

After You Install Everything, Follow This Steps

1. Make Folder (Folder Name Examples "Toolkit")

2. Open CMD And Open Toolkit Folder In CMD

```
cd ~/Documents/Toolkit
```

4. Copy This Command To CMD (If This Doesn't Work You Can Use Git CMD)

```
git clone https://github.com/HaHmada/Toolkit-To-Install-TWRP-For-Certus.git -b TWRP
```

5. Open Notepad++, And Paste In Notepad++

```
@echo off
TITLE Toolkit Flash TWRP By HaH Mada
color 37
Mode con: COLS=75 LINES=40
echo.
echo     ************************************************************
echo     *******           Toolkit Flash OrangeFox            *******
echo     *******                 By HaH mada                  *******
echo     ************************************************************
echo     *******                 Redmi 6/6A                   *******
echo     ************************************************************
echo.             
echo.
taskkill /f /im "adb.exe" >nul 2>nul
cd /d %~dp0adb
adb kill-server
adb start-server
echo.
echo   *******  Waiting For The Device
adb devices
echo.
pause
echo.
echo   *******  Booting Into Fastboot Mode
adb reboot bootloader
echo.
pause
echo.
echo   *******  Erase Stock Recovery
fastboot erase recovery
echo.
pause
echo.
echo   *******  Flashing Twrp Recovery
fastboot flash recovery recovery.img
echo.
pause
echo.
echo   *******  Reboot To Recovery
fastboot boot recovery.img
echo.             
echo   *******  SUCCESS!
echo   If You Can't Enter TWRP, Enter TWRP Manually With Volume Up + Power   
echo.                
ECHO.  Press ENTER to exit ...
pause  >NUL
EXIT
```

6. Once you are done, click CTRL+SHIFT+S & Following This Settings

File name: Toolkit.bat

Save as type: All types (*.*)

7. Finish You Can Use This Toolkit
