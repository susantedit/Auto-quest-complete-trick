# Discord Auto Quest Complete

A step-by-step guide to automatically complete Discord quests using the developer console.

---

### Step 1: Download and Install Discord
You need the official Discord desktop client for Windows. The web browser version will not work for game or stream quests.
- Download link: https://discord.com/download
- Run the installer and sign in to your Discord account.

---

### Step 2: Enable Discord Developer Tools
Discord disables the inspection console by default. You need to turn it on via your local Discord settings file:

1. Press `Win + R` on your keyboard to open the Windows Run dialog.
2. Type `%appdata%/discord/` and press **Enter**. A folder will open in File Explorer.
3. Find the file named `settings.json`.
4. Download [`setting.json`](./setting.json) from this repository and replace the existing `settings.json` file in that folder. If it doesn't replace, open `settings.json` in Notepad, paste the content from `setting.json`, and save.

---

### Step 3: Fully Restart Discord
The new setting only takes effect after Discord reloads:

1. Close Discord.
2. Open Task Manager (`Ctrl + Shift + Esc`), find any running Discord processes, and end them (or simply restart your computer).
3. Open Discord again.

---

### Step 4: Accept Your Quests
1. Open Discord and go to **User Settings** (the gear icon at the bottom left).
2. Click on the **Quests** tab (or **Gift Inventory**).
3. Click **Accept Quest** on every quest you want to finish.

---

### Step 5: Open DevTools and Allow Pasting
1. While Discord is open, press `Ctrl + Shift + I` to open Developer Tools.
2. Click the **Console** tab at the top.
3. If Discord displays a warning that blocks pasting, type:
   ```text
   allow pasting
   ```
   and press **Enter**.

---

### Step 6: Run the Script
1. Open `dc script.txt` from this repository and copy the entire code.
2. Paste it into the Discord Console tab and press **Enter**.
3. The script will automatically spoof progress for all accepted quests:
   - **Video quests:** Automatically completes in small steps.
   - **Game play quests:** Emulates the game process until the required time is reached.
   - **Stream quests:** Emulates a stream to any voice channel (make sure at least one other user is in the voice channel with you).
4. Leave Discord open until the console displays that the quests are completed.
