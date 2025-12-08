# **Starforged Architect \- User Manual**

## **Overview**

The **Starforged Architect** is an offline, browser-based sector generator designed for the *Ironsworn: Starforged* TTRPG. It generates procedural star systems, visualizes them on a hex grid, creates trade routes ("Space Lanes"), and populates settlements with unique NPCs.

Because it runs entirely in your browser, **no internet connection is required** once you have the file.

## ---

**1\. Getting Started**

1. **Launch:** Simply double-click the ```architect.html``` file. It will open in your default web browser.  
2. **Navigation:** Use the **Sidebar** (on the left) or the **Menu Button** (top-left on mobile) to control the generator.  
3. **Generate:** Select a Region type (**Terminus**, **Outlands**, or **Expanse**) and click **SCAN** to generate a new sector.

## ---

**2\. Managing the Database (CSV Import)**

The Architect comes with a default database, but it is designed to be customized with your own creative tables.

### **How to Import Data**

1. Create or edit a spreadsheet (Excel, Google Sheets, etc.).  
2. Save/Export the specific tab as a **CSV (Comma Separated Values)** file.  
3. Drag and drop the CSV file into the **"Drop CSV files here"** box in the sidebar.  
4. The system will confirm the update. Your custom data is saved to your browser's **Local Storage**, so it will persist even if you close the browser.

### **Resetting Data**

If you make a mistake or want to return to the original tables, click the **RESET** button next to the status indicator.

### **Required CSV Headers**

The system recognizes data based on the **Header Row** (the first row of your CSV). 
What you name the CSV file does not matter as the **Header Row** determine how the code processes the information.

Ensure your columns use these **exact** names in your Header Row:

* Sector Name Prefix, Sector Name Suffix  
* Stellar Object, Stellar Desc, Stellar Wiki  
* Planet Name, Planet Desc, Planet Habitable, Planet Wiki  
* Settlement Name Prefix, Settlement Name Suffix  
* Settlement Location, Location Desc  
* Settlement Population, Settlement Authority, Settlement Economy  
* NPC First Name, NPC Surname, NPC Descriptor  
* Ship Name, Visitor Type

## ---

**3\. Exporting & Saving**

### **Capturing the Map**

Click the **CAPTURE MAP** button in the sidebar.

* This generates a high-resolution PNG image.  
* **Smart Legend:** The image includes an expanded sidebar on the right that is *not* visible on the main screen. This legend contains the full dossier for the sector, including planet descriptions, settlement demographics, and debris field warnings.

### **Exporting NPC Profiles**

When you select a Settlement on the map, the "Active Traffic" list appears in the sidebar.

* Look for the small **\[⇩ TXT\]** button next to a Captain's name.  
* Clicking this will download a .txt file containing that specific NPC's profile, ship details, and stat block, ready to be pasted into your campaign notes.

## ---

**4\. Technical Logic & Rules**

### **Hardcoded Essentials**

To ensure the visual engine functions correctly, specific **Stellar Objects** are hardcoded into the logic. If your custom CSV omits them, the system will re-inject them to prevent crashes. These are required for specific visual effects:

* **Black Hole:** Triggers the "Event Horizon" safety zone logic and specific gravitational lensing visuals.  
* **Nebula:** Triggers the gas cloud background layers.  
* **Protoplanetary Disk:** Triggers the "Debris Field" logic and restricts settlements to orbital stations.  
* **Yellow Dwarf:** Ensures there is always at least one "Standard Star" type available.

### **Duplicate Handling**

The system includes a sanitizer that runs during data import:

* **Automatic Deduplication:** If your CSV contains duplicate entries (e.g., "Ironhold" listed three times), the system automatically filters them down to a single entry.  
* **Unique Name Enforcement:** During generation, the system maintains a "Registry" of used names for the current sector. It will attempt to re-roll up to 50 times to prevent two planets or settlements from having the exact same name in the same system.

### **Space Lanes & Transit Sectors**

* **Space Lanes:** Yellow dashed lines represent established trade routes. They are calculated using a pathfinding algorithm that connects the Entry Gate, all Settlements, and the Exit Gate. The pathfinder actively attempts to route *around* dangerous celestial bodies (like Black Holes).  
* **Transit Sectors:** Depending on the region selected, there is a chance to generate a "Transit Sector." These are largely empty systems meant for travel, containing only 0 or 1 settlements (usually a Waystation), emphasizing the vastness of the Forge.
