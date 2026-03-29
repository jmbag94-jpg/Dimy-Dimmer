
<img width="304" height="430" alt="image" src="https://github.com/user-attachments/assets/a202bc34-caac-4552-a8b4-dca8a2eaa579" />
<img width="307" height="427" alt="image" src="https://github.com/user-attachments/assets/e64d00c9-cc05-4249-91af-39dd4b4fa66f" />
<img width="301" height="421" alt="image" src="https://github.com/user-attachments/assets/2e7559ea-1838-420b-b2c4-84dc0ad6b704" />
<img width="301" height="427" alt="image" src="https://github.com/user-attachments/assets/e1b09a9a-ea9e-4e8a-b221-05e8faa591d1" />

Dear user, I introduce you the free-of-charge Dimy-Dimmer application that I created with the help of AI.
This application will let you make your screen darker or brighter.
What makes this application different from other dimmer applications are:
1. When you make your screen dark and when you take a screenshot or record a video, the outcome will not come out as dark as you see in your screen.
2. The dimmer works even when you use fullscreen applications or games.
3. You will be able to change dim level with only one hand (Alt Gr + Up/Down arrow).

HOW TO INSTALL:
If launching the .exe file doesn't work, you will need to compile the application via either w64devkit or Visual Studio Build Tools.

METHOD 1: w64devkit  

  STEP 1: Download w64devkit
    1. Go to: https://github.com/skeeto/w64devkit/releases
    2. Download the file: w64devkit-x64-2.1.0.zip
       (or the latest version)

  STEP 2: Extract the zip
    1. Right-click the downloaded zip
    2. Click "Extract All..."
    3. Extract to any location, e.g. C:\w64devkit

  STEP 3: Open the compiler terminal
    1. Open the extracted folder
    2. Double-click: w64devkit.exe
    3. A black terminal window opens

  STEP 4: Go to your Dimmer folder
    1. Type:  cd "
    2. Open File Explorer, go to the folder with dimmer.c (or just hold the folder and drag it to w64devkit, skip to 5th step)
    3. Click the address bar and copy the path 
    4. Right-click in the terminal to paste the path
    5. Type the closing "  and press Enter

    Example:
       cd "C:\Users\YourName\Desktop\Dimmer"

  STEP 5: Build
    Copy this line, then right-click in the terminal
    to paste it by right click, then press Enter:

gcc -o Dimmer.exe dimmer.c -mwindows -municode -lcomctl32 -lshell32 -luser32 -lgdi32 -ladvapi32 -lole32 -static -O2

    When you see the cursor on a new line with no
    errors, it worked!

  STEP 6: Run
    Double-click Dimmer.exe in your folder!

METHOD 2: Visual Studio Build Tools

  STEP 1: Download
    Go to: https://visualstudio.microsoft.com/visual-cpp-build-tools/
    Click "Download Build Tools" and run the installer

  STEP 2: Install
    Check "Desktop development with C++" and click Install
    (takes 10-20 minutes)

  STEP 3: Open the compiler terminal
    Click Start, search for "x64 Native Tools Command Prompt"

  STEP 4: Go to your Dimmer folder
    Type:  cd /d "C:\path\to\your\Dimmer\folder"

  STEP 5: Build
    Paste this line and press Enter:

cl /O2 /DUNICODE /D_UNICODE dimmer.c /Fe:Dimmer.exe /link /SUBSYSTEM:WINDOWS user32.lib gdi32.lib shell32.lib comctl32.lib advapi32.lib ole32.lib

  STEP 6: Run
    Double-click Dimmer.exe!
    (You can delete dimmer.obj - not needed)

FAQ
Q: Cannot paste with Ctrl+V while compiling?
A: Right-click in the terminal to paste

Q: Can't get higher dim level more than 50%?
A: That's a Windows security limitation, it caps how far gamma ramps can deviate from the default (typically 50%). You can unlock the full range (up to 95%) by going "Debug" tab and click "Unlock Full Range" button. Windows will ask for Administrator permission, click Yes. Restart PC. Now you will be able to Dim your screen max 95%.

Q: Is it detrimental to my any hardware to do up to %95 dimming?
A: No, it's completely safe for your hardware. The gamma ramp is purely a software lookup table that sits between your graphics card's frame buffer and the display output signal. It changes the numbers being sent to your monitor, not anything physical. It's the same mechanism Windows uses for Night Light (the blue light filter) or color calibration profiles.

If you find this application useful and want to make my day, I will gladly accept any form of donation. I thank you in advance!

Disclaimer: This software is free to download, use, modify, and distribute. This software is provided 'as-is' and 'as-available' without warranty of any kind. We do not guarantee that the software will be error-free or compatible with all systems. Any reliance you place on such information is strictly at your own risk. We will not be liable for any losses or damages in connection with the use of our app.

