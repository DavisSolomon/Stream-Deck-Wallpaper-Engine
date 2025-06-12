📁 Wallpaper Tool - Stream Deck Wallpaper Switcher
------------------------------------------------------

🎯 What This Tool Does:
This tool lets you instantly switch your Wallpaper Engine background by pressing a Stream Deck button. You can:
- Assign one button per wallpaper
- Choose which monitor the wallpaper appears on
- Play a random wallpaper to a specific monitor

This gives you fast, customizable control without needing to open Wallpaper Engine manually.

---------------------------
🛠️ SETUP INSTRUCTIONS
---------------------------

1️⃣ STEP 1: Edit the config.txt File

Inside the folder you received, there is a file called:
  config.txt

Open it and change the first line to your **Wallpaper Engine executable path**.

Example:
  E:\SteamLibrary\steamapps\common\wallpaper_engine\wallpaper32.exe

To find yours:
- Open Steam
- Right-click Wallpaper Engine → Manage → Browse local files
- Copy the full path to wallpaper32.exe and paste it into `config.txt`

Make sure there are no extra "quotes" except the ones already there and only one path per line.

--------------------------------------------------------------
2️⃣ STEP 2: Find the Wallpaper JSON Path You Want to Use
--------------------------------------------------------------

Each wallpaper has a `.json` file that tells Wallpaper Engine how to load it.

To get the path:

1. Open Wallpaper Engine
2. Right-click the wallpaper you want
3. Click **"Open in Explorer"**
4. In the folder that opens, find the file called:  
   `project.json`
5. Click it Once and then Right-click the file → choose **"Copy as Path"**

This gives you the full `.json` path you’ll use in the next step.

🧠 Note:
Wallpaper Engine’s Workshop content is stored under this folder: [Steam path]\steamapps\workshop\content\431960\

`431960` is the Workshop ID for Wallpaper Engine — you’ll find all your subscribed wallpapers inside it.

--------------------------------------------------------------
3️⃣ STEP 3: Create a Stream Deck Button
--------------------------------------------------------------

1. Open the Elgato Stream Deck software
2. Drag a “System → Open” action onto a button
3. In the **App / File** field:
   → Browse and select `Wallpaper_Tool.exe` (from this folder)
4. Add your Arguments after you have pasted your directory for the Wallpaper_Tool.exe
5. In the **Arguments** field, paste the path to your `project.json` wallpaper file

Example: "C:\Users\tripp\Downloads\Wallpaper_Tool\Wallpaper Tool.exe" "Path\To\Wallpaper\Here.json" 0

✅ Make sure the path is in "quotes", especially if it contains spaces.

6. (Optional) Set a Title or Icon for the button to match the wallpaper.

That’s it! The button will now load that wallpaper when clicked.

--------------------------------------------------------------
🌀 OPTIONAL: Play a Random Wallpaper
--------------------------------------------------------------

You can make a Stream Deck button that plays a random wallpaper from your library.

To do this:

1. add the --random argument to your stream deck
2. It will look something like this: "C:\Users\tripp\Downloads\Wallpaper_Tool\Wallpaper_Tool.exe" --random 0

💡 This will randomly pick one of the `project.json` files inside subfolders of the path.

--------------------------------------------------------------
🖥️ OPTIONAL: Change Which Monitor the Wallpaper Loads On
--------------------------------------------------------------

To set a specific monitor (if you have multiple), add this to the END of your argument:

All you need to do is add a number to your argument.

Monitor numbers usually go like this:
- 0 = Primary monitor
- 1 = Second monitor
- 2 = Third monitor (if applicable) and so on and so forth

Test which one matches your setup.

If you do not add a argument for a monitor then it will fallback onto the monitor you have specified in the config file
--------------------------------------------------------------
📂 FILES INCLUDED IN THIS FOLDER:
--------------------------------------------------------------

- Wallpaper_Tool.exe      ← The wallpaper launcher
- config.txt            ← Holds your Wallpaper Engine path
- README.txt            ← This instruction file

--------------------------------------------------------------
❗ COMMON ISSUES:
--------------------------------------------------------------

- If nothing happens when you click the button:
  - Make sure the `config.txt` has the correct path to `wallpaper32.exe`
  - Make sure the `.json` path is correct (you can test it manually in CMD)
  - Make sure your Stream Deck arguments are inside **quotes**

- If wallpapers are loading on the wrong screen:
  - Add `0-∞` to the end of the argument - See Earlier "🖥️ OPTIONAL" For Explanation

--------------------------------------------------------------
🎉 ENJOY!
--------------------------------------------------------------

You now have full Stream Deck control of your dynamic wallpapers.  
Customize, theme, and switch instantly with ease.

Made with ❤️ by Solomon and ᶜʰᵃᵗᴳᴾᵀ

Authors Note: I apologize if this doesn't meet your standards. I have no experience in coding but I wanted something like this for my stream deck so I decided to try and use ChatGBT to create it. Ive gone through a few hours of getting everything to work so I hope you enjoy it. Enjoy :)
