# OPL PS1 AIO Converter GUI

An all-in-one Windows application for preparing and installing **PlayStation 1 games** for **POPStarter** on the PlayStation 2.

---

# Features

* 🎮 Convert PS1 BIN/CUE backups into POPStarter VCD files
* 📦 Automatic ZIP extraction
* 💿 Automatic multi-track BIN merging
* 💾 Install games for USB, MX4SIO, MMCE, exFAT HDD, SMB and APA Internal HDD
* 🛠 Apply Cheats
* 📺 Apply HDTVFIX patches
* 📥 Download missing CFG / Metadata
* 🖼 Download missing ART files
* 📐 Apply Aspect Ratio patches where available
* 🗂 Built-in APA HDD Transfer Tool
* ➕ Create POPS Partition directly from the GUI
* 🌐 SMB Driver Editor for IPCONFIG.DAT and SMBCONFIG.DAT
* 🧹 Cleanup utility for working directories
* ⚡ Modern graphical interface with batch conversion support
* 🔄 Built-in automatic update system

---

# Before You Begin

## POPStarter Runtime Files

For **USB, MX4SIO, MMCE, exFAT HDD and SMB** installations, the following POPStarter runtime files are required:

```text
POPSTARTER.ELF
POPS_IOX.PAK
```

These files are **copyrighted and will NOT be provided with this application**.

You must obtain these files separately and place them inside the `POPS` folder on your target storage device.

For example:

```text
POPS
├── POPSTARTER.ELF
└── POPS_IOX.PAK
```

> **Important:** These runtime files are required for POPStarter to function correctly. They are not included with the application.

---

## APA Internal HDD Runtime Files

APA Internal HDD installations use a different set of runtime files.

The required files are:

```text
POPS.ELF
POPS.PAK
IOPRP_252.IMG
```

These files are **copyrighted and will NOT be provided with this application**.

You must obtain these files separately before transferring the POPS runtime to your APA HDD.

---

## POPStarter Drivers

The required **POPSTARTER PS2 drivers** are included with this application.

They can be found inside the included:

```text
Resources
└── Popstarter PS2 Drivers
```

Inside this folder, you will find the **POPSTARTER** folder.

### Installation

1. Copy the entire **POPSTARTER** folder to your USB flash drive or memory card.
2. Launch **uLaunchELF** on your PlayStation 2.
3. Copy the **POPSTARTER** folder to:

```text
mc0:/
```

The final location should be:

```text
mc0:/POPSTARTER/
```

This only needs to be done **once for each memory card**.

> **Note:** These drivers are included with the application, while the copyrighted POPStarter runtime files listed above are not.

---

# Resources Folder

The application is distributed with a **Resources** folder containing the tools and files required by the converter.

For new users, the recommended folder structure is:

```text
OPL PS1 AIO Converter
├── OPL_PS1_AIO_Converter_GUI.exe
├── Updater.exe
└── Resources
```

The application automatically detects the included **Resources** folder.

**You do not need to manually select the Resources folder inside the application.**

> **Important:** Keep the `Resources` folder next to the converter EXE. Do not rename or remove it.

---

# 🎮 Game Converter

The **Game Converter** converts PlayStation 1 backups into **POPStarter-compatible VCD files**.

## Supported Formats

* BIN/CUE
* Multi-track BIN/CUE
* ZIP archives containing BIN/CUE games

---

## Step 1 — Source Folder

Browse to the folder containing your PlayStation 1 games.

The converter automatically scans **all subfolders recursively**.

---

## Step 2 — Output Folder

Select where your converted **VCD** files should be saved.

For **USB, MX4SIO, MMCE, exFAT HDD and SMB**, you can select the `POPS` folder on your target device.

Example:

```text
USB:\POPS
```

or:

```text
PS2SMB\POPS
```

For **APA Internal HDD**, do **not** select a folder on the HDD.

Instead, create a temporary working folder on your PC.

For example:

```text
D:\PS1_Conversion\
└── POPS
```

Then select the **POPS folder inside that temporary folder** as your Output Folder.

Your workflow should therefore look like:

```text
D:\PS1_Conversion\
└── POPS
    ├── GAME1.VCD
    ├── GAME2.VCD
    └── GAME3.VCD
```

This temporary `POPS` folder will contain the converted VCD files that will later be transferred to your APA HDD using the **Transfer to HDD** tool.

> **Important:** For APA installations, the Output Folder should be the temporary `POPS` folder you created on your PC, not the physical PS2 HDD.

---

## Step 3 — Scan

Click **Scan for Games**.

The program will automatically detect all supported games.

---

## Step 4 — Select Games

Choose which games you wish to convert.

You can convert:

* A single game
* Multiple games
* Your entire library

---

## Step 5 — Convert

Click **Convert Selected**.

The converter automatically:

* Extracts ZIP archives
* Merges multi-track BIN games
* Converts games into POPStarter VCD format

Once completed, your VCD files are ready to install.

---

# 💾 USB / MX4SIO / MMCE / exFAT HDD

Use this tab when playing PS1 games from:

* USB Flash Drive
* MX4SIO
* MMCE
* exFAT External HDD

---

## Required Runtime Files

Copy the following copyrighted runtime files into the **POPS** folder on your storage device:

```text
POPSTARTER.ELF
POPS_IOX.PAK
```

These files are **not provided with this application**.

Example:

```text
POPS
├── POPSTARTER.ELF
├── POPS_IOX.PAK
└── GAME.VCD
```

---

## PS2 Data Folder

Select the **ROOT** of your USB/SD Card/exFAT HDD.

The ROOT is the folder containing the standard OPL directory structure.

Example:

```text
APPS
ART
CFG
CHT
CD
DVD
POPS
THM
VMC
```

Do **not** select the POPS folder itself.

---

## Options

### Apply Cheats

Applies available cheat patches to supported PS1 games.

---

### Apply HDTVFIX

Enable this option if you're using:

* PS2 to HDMI adapters
* HDMI converters
* Modern televisions
* Computer monitors

---

### Download CFG / Metadata

Downloads available metadata files for supported games.

---

### Aspect Ratio

Applies available Aspect Ratio patches created by **Hugopocked**.

---

## Run

Click **Run** to process and install your selected games.

Once complete:

1. Safely remove your storage device.
2. Connect it to your PlayStation 2.
3. Enable the **APPS** page inside OPL Settings.
4. Launch your games using POPStarter.

---

## ⬇️ Download Missing ART / CFG

The USB tab includes **down-arrow buttons** for downloading missing artwork and CFG files.

These buttons are especially useful if the artwork or CFG server is temporarily unavailable when you initially install your games.

If some artwork or CFG files could not be downloaded:

1. Complete your installation normally.
2. Later, when the server is available again, reconnect your storage device to your PC.
3. Use the corresponding **download arrow button** to download the missing files.

This allows you to download missing artwork or CFG files at a later time without having to reinstall or reconvert your games.

---

# 🌐 SMB

Use this tab when storing your PlayStation 1 games on an SMB network share.

---

## Required Runtime Files

Copy the following copyrighted runtime files into your SMB **POPS** folder:

```text
POPSTARTER.ELF
POPS_IOX.PAK
```

These files are **not provided with this application**.

Example:

```text
POPS
├── POPSTARTER.ELF
├── POPS_IOX.PAK
└── GAME.VCD
```

---

## PS2 Data Folder

Select the **ROOT** of your SMB share.

Example:

```text
APPS
ART
CFG
CHT
CD
DVD
POPS
THM
VMC
```

Do **not** select the POPS folder itself.

---

## Edit POPS SMB Drivers

The SMB tab includes a built-in **Edit POPS SMB Drivers** button that allows you to configure the network settings used by POPStarter when loading PS1 games over SMB.

This tool edits two configuration files:

* `IPCONFIG.DAT` – PS2 network settings
* `SMBCONFIG.DAT` – SMB server settings

### IPCONFIG.DAT

Configure:

* PS2 IP address
* Netmask
* Gateway

### SMBCONFIG.DAT

Configure:

* PC/server IP address
* SMB port
* Share name
* Username
* Password

### How to Use

1. Click **Edit POPS SMB Drivers**.
2. A new window will open with two tabs:

   * **IPCONFIG.DAT**
   * **SMBCONFIG.DAT**
3. Enter your network and SMB server information.
4. Click **Restore Defaults** if you want to reset the fields.
5. Click **Save** to write the configuration files.
6. Follow the instructions shown by the application to deploy the POPSTARTER folder to your memory card.

> **Note:** Leave the **SMB Port** field blank to use the default SMB port (`445`). Only specify a port if your SMB server uses a different port.

---

## Options

### Apply Cheats

Applies available cheat patches.

---

### Apply HDTVFIX

Recommended when using:

* HDMI adapters
* HDMI converters
* Modern displays

---

### Download CFG / Metadata

Downloads available CFG and metadata files.

---

### Aspect Ratio

Applies available Aspect Ratio patches created by **Hugopocked**.

---

## Run

Click **Run** to process and install your selected games.

After completion:

1. Refresh your SMB share if necessary.
2. Launch Open PS2 Loader.
3. Enable the **APPS** page.
4. Launch your PlayStation 1 games.

---

## ⬇️ Download Missing ART / CFG

The SMB tab also includes **down-arrow buttons** for downloading missing artwork and CFG files.

If some files could not be downloaded during the initial installation because the download server was unavailable, you can download them later.

Simply reconnect to your SMB share when the server is available and use the corresponding **download arrow button** to retrieve the missing files.

There is no need to reconvert or reinstall the games.

---

# 💿 APA (Internal HDD)

Use this tab if you want to install your PlayStation 1 games directly onto an **APA-formatted internal PS2 HDD**.

Unlike USB and SMB, games are first converted into VCD files on your PC and then transferred to the HDD.

---

## ⚠️ Prerequisites

### Run as Administrator

The APA HDD transfer tool requires administrator privileges to access physical drives and mount partitions.

Always launch the application as Administrator when using the APA tab.

* Right-click the `.exe` → **Run as administrator**
* Or set the `.exe` to always run as administrator in **Properties → Compatibility**

If you don't run the application as administrator, the HDD list may be empty and transfers may fail.

---

# Step 1 — Create a POPS Partition

Before transferring games, your HDD must contain at least one POPStarter partition, such as:

```text
__.POPS0
```

## Using the Built-in Create POPS Partition Tool

1. Click **Transfer to HDD** in the APA tab.
2. Click **Connect** and select your PS2 HDD.
3. If no `__.POPS` partitions exist, you will see a warning.
4. Click **Create POPS Partition**.
5. Choose a partition size using the slider or numeric input.
6. Click **Create**.
7. The tool will create the partition and automatically format it as PFS.

Once created, the partition will appear in the list and will be ready for transferring games.

> **Note:** POPS partitions can be created up to **128 GB** per partition.

---

# Step 2 — Prepare the APA Runtime Files

APA installations require the following copyrighted runtime files:

```text
POPS.ELF
POPS.PAK
IOPRP_252.IMG
```

These files are **not provided with this application**.

Place the files into:

```text
Resources
└── APA HDD Binaries
```

The application will automatically detect them from the included Resources folder.

> **Important:** These files must be obtained separately because they are copyrighted.

These files only need to be transferred once unless the POPS partition is recreated.

---

# Step 3 — Create a Temporary Working Folder

For APA installations, create a temporary working folder anywhere on your PC.

Inside that folder, create a folder named:

```text
POPS
```

For example:

```text
D:\PS1_Conversion\
└── POPS
```

The `POPS` folder is where the converter will place your converted VCD files.

---

# Step 4 — Convert Your Games

Open the **Game Converter** tab.

Select:

* **Source Folder** → Your BIN/CUE or ZIP backups
* **Output Folder** → The temporary `POPS` folder you created in Step 3

For example:

```text
D:\PS1_Conversion\POPS
```

You do **not** need to select the Resources folder. The application automatically detects it.

Click:

* **Scan for Games**
* Select the games you want
* **Convert Selected**

Once finished, your temporary POPS folder will contain the converted VCD files.

Example:

```text
D:\PS1_Conversion\
└── POPS
    ├── GAME1.VCD
    ├── GAME2.VCD
    └── GAME3.VCD
```

> **Important:** This is only a temporary working folder on your PC. The games will later be transferred from this folder to the APA HDD.

---

# Step 5 — Prepare the Installation

Open the **APA (Internal HDD)** tab.

Choose any desired options:

* Apply Cheats
* Apply HDTVFIX
* Download CFG / Metadata
* Aspect Ratio patches

Click **Run**.

The application will prepare the games in your temporary POPS folder.

---

# Step 6 — Transfer to the HDD

Click **Transfer to HDD**.

A new window will open.

1. Select your PlayStation 2 HDD from the drop-down list.
2. Click **Connect**.
3. Click **Transfer Binaries** if required.
4. Click **Start Transfer**.

The program will copy your converted games directly to the selected POPS partition.

If the APA runtime files have already been installed, the application will indicate that they are already installed.

---

# Additional APA Tools

## Download Missing ART

Downloads missing cover artwork for games already installed on the HDD.

---

## Download Missing CFG

Downloads missing CFG files for installed games.

---

## Create POPS Partition

Creates a new `__.POPS` partition on the HDD.

The tool handles the required APA sub-partitioning and PFS formatting automatically.

---

## Cleanup

The **Cleanup** button clears the temporary working POPS directory, making it easy to prepare for your next batch of conversions.

---

# Finished

Once the transfer is complete:

1. Close the Transfer window.
2. Exit the application.
3. Connect the HDD to your PlayStation 2.
4. Launch Open PS2 Loader.
5. Enable the **APPS** page in OPL Settings.
6. Launch POPStarter and enjoy your PlayStation 1 games.

---

# 🔄 Automatic Updates

The application includes a built-in update system.

When a new version is released, the application can check the project's GitHub release page for a newer version.

If an update is available:

1. The application will notify you that a newer version is available.
2. You can choose whether to download it.
3. The updater downloads the new application directly from the official GitHub release.
4. The downloaded EXE is verified using its **SHA-256 checksum**.
5. The current application is safely replaced.
6. The newly installed version is verified again.
7. The updated application is launched automatically.

> **Note:** The automatic updater only replaces the main application EXE. Your `Resources` folder and other files are not removed or modified during a normal application update.

For new users, download the latest complete release package, extract it, and run:

```text
OPL_PS1_AIO_Converter_GUI.exe
```

The complete package includes:

```text
OPL_PS1_AIO_Converter_GUI.exe
Updater.exe
Resources\
```

Keep these files together.

---

# Notes

* ZIP archives are extracted automatically during conversion.
* Multi-track games are merged automatically.
* Existing VCD files will not be overwritten unless **Overwrite Existing VCD Files** is enabled.
* The converter scans all subfolders recursively.
* Always keep a backup of your original PlayStation 1 games.
* APA POPS partitions up to **128 GB** can be created directly from the GUI.
* SMB network settings can be edited directly from the application using the built-in **Edit POPS SMB Drivers** tool.
* For USB, MX4SIO, MMCE, exFAT HDD and SMB, the required runtime files are `POPSTARTER.ELF` and `POPS_IOX.PAK`.
* For APA Internal HDD, the required runtime files are `POPS.ELF`, `POPS.PAK` and `IOPRP_252.IMG`.
* All copyrighted runtime files listed above are **NOT provided** with this application.
* The `Resources` folder is automatically detected and should remain next to the converter EXE.
* The application and updater are designed for **Windows x64**.

---

# ❤️ Credits

## OPL PS1 AIO Converter GUI

Created by **Eliminator14 (Pixel)**

---

## Special Thanks

* Hugopocked
* GDX
* uyjulian
* KrHACKen
* Ripto
* Berion
* Shaolin Assassin
* El_Isra
* BeardedKraken13
* R3Z3N
* Gledson999
* Chris Putnam

A huge thank you to everyone in the PlayStation 2 homebrew community whose work, research, testing, documentation, and tools have helped keep the PS2 scene alive.

Without your contributions, projects like this would not have been possible.

---

# 🎮 Enjoy!

Enjoy your PlayStation 1 library on the PlayStation 2!

**Happy Gaming! 🎮**
