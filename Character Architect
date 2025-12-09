# Starforged Character Architect - User Manual

## Overview
The **Character Architect** is an offline, browser-based character sheet and asset manager for *Ironsworn: Starforged*. It combines automated rules logic (like Momentum resets and XP calculation) with a flexible asset library that allows for custom content.

Because it runs entirely in your browser, **no internet connection is required** once you have the file.

---

## 1. Getting Started
1.  **Launch:** Double-click the `character.html` file. It will open in your default web browser.
2.  **Creation Wizard:** On first load, you will be greeted by the **Identity Wizard**.
    * **Step 1:** Enter your Name, Pronouns, Look, and Background Vow.
    * **Launch:** Click "Launch System" to enter the main Dashboard.
    * *Note: Stats are assigned manually on the Dashboard using the Standard Array (3, 2, 2, 1, 1).*

---

## 2. The Dashboard Interface

### Identity & Portrait
* **Portrait:** The square box in the center of the header is your portrait area.
    * **Click** the box to upload an image from your device.
    * *Note: The image data is saved inside your character save file, so it allows you to move your character between devices.*
* **Save/Load:** Located in the top right. This saves your character data to a `.json` file (Cartridge) or loads one you previously saved.

### Stats & Meters
* **Stats:** Enter your stats (Edge, Heart, Iron, Shadow, Wits) in the input boxes. Remember the standard array: **3, 2, 2, 1, 1**.
* **Meters (Health, Spirit, Supply):**
    * **Left-Click (or Tap):** Increases the value (+1).
    * **Right-Click (or Long Press):** Decreases the value (-1).
* **Momentum:**
    * This track is automated based on your Impacts.
    * **Blue Number:** Your current Momentum.
    * **White Bar:** Your current Reset value.
    * **Red Triangle:** Your current Max Momentum.

### Impacts
* Toggle the buttons (**Wounded, Shaken, Doomed, etc.**) to mark them.
* **Automation:** Marking impacts automatically adjusts your **Max Momentum** (10 minus impacts) and your **Momentum Reset** (+2, +1, or 0) according to the rules.

---

## 3. Asset Management

### Adding Assets
1.  Go to the **Asset Library** box (bottom right).
2.  Select an asset from the dropdown menu (e.g., *[Command Vehicle] Starship*).
3.  Click the **[ + ]** button.
4.  The asset will appear in your list with the **first ability automatically unlocked**.

### Using Assets
* **Custom Fields:** You can rename assets (e.g., change "Starship" to "The Ebon Hawk") and use the bottom input fields for Notes or Cargo.
* **Abilities:** Check the boxes to unlock abilities.
* **Health Track:**
    * If an asset has health (like a Vehicle or Companion), a track appears.
    * **Click** a pip to set the health level.
* **Vehicle Troubles:**
    * If you add a Vehicle, you will see toggles for **Battered** and **Cursed**.
    * **Battered:** If marked, the asset's Health Track becomes **Locked** (red/dimmed) and cannot be changed until you repair the vehicle and uncheck Battered.
    * **Cursed:** Marking this (or Battered) counts towards your total Impacts, lowering your Momentum Max/Reset.
* **Companions:**
    * Companions have an **Out of Action** toggle. Marking this dims the card to show it cannot be leveraged.

### Managing the Library (Custom Assets)
You are not limited to the default assets. You can import your own or delete ones you don't use.

* **Deleting from Library:** Select an asset in the dropdown and click the **Trash Can [🗑️]** button. *Warning: This permanently removes it from your browser's local storage.*
* **Importing via CSV:**
    1.  Create a CSV file with the following headers in the first row:
        `Category, Name, Ability 1, Ability 2, Ability 3, Max Health`
    2.  Drag and drop the file into the **"Drop Assets.csv here"** box.
    3.  The system will **append** these new assets to your library (skipping duplicates).

---

## 4. Progress & Legacies

### Progress Tracks
Use this section for Iron Vows, Combat, Expeditions, and Connections.
1.  **Create:** Enter a Name, select a Type, and choose a **Rank** (Troublesome to Epic). Click **ADD**.
2.  **Marking Progress:**
    * Click **[+ Mark]** to add progress. The system automatically calculates how many ticks to add based on the Rank (e.g., Dangerous adds 2 full boxes, Epic adds 1 single tick).
    * Click **[ - ]** to undo progress if you made a mistake.

### Background Vow
Your Background Vow is permanently pinned. It functions as an **Epic** track (1 tick per mark).

### Legacies & XP
* **Interaction:**
    * **Left-Click:** Adds a tick.
    * **Right-Click:** Removes a tick.
* **XP Calculation:**
    * The system automatically calculates **XP Earned** (2 XP per fully filled box across all three Legacy tracks).
    * Enter the amount you have used in the **Spent** box to see your **Available XP**.

---

## 5. Saving Your Data
The Architect uses a "Cartridge" system.
* **Manual Save:** Always click **[SAVE]** at the end of a session. This downloads a `.json` file to your computer containing your character, assets, tracks, and portrait.
* **Local Storage:** Your **Asset Library** (the list of available cards) is saved to your browser's storage, so your custom assets will be there the next time you open the tool.
