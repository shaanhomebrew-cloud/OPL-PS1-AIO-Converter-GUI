# OPL PS1 AIO Converter GUI

An all-in-one Windows application for preparing and installing **PlayStation 1 games** for **POPStarter** on the PlayStation 2.

---

# Features

* 🎮 Convert PS1 BIN/CUE backups into POPStarter VCD files
* 📦 Automatic ZIP extraction
* 💿 Automatic multi-track BIN merging
* 💾 Install games for USB, MX4SIO, MMCE, exFAT HDD (GPT/MBR), SMB and APA Internal HDD
* 🛠 Apply Cheats
* 📺 Apply HDTVFIX patches
* 📥 Download missing CFG / Metadata
* 🖼 Download missing ART files
* 📐 Apply Aspect Ratio patches where available
* 🗂 Built-in APA HDD Transfer Tool
* ➕ Create POPS partitions directly from the GUI
* 🌐 SMB Driver Editor for IPCONFIG.DAT and SMBCONFIG.DAT
* 🧹 Cleanup utility for working directories
* ⚡ Modern graphical interface with batch conversion support
* 🔄 Built-in update system

---

# Before You Begin

## POPStarter PS2 Drivers

The application includes the required **POPStarter PS2 drivers** inside the `Resources` folder.

However, whether you need to install them depends on the method you are using.

### FAT32 USB and APA Internal HDD

**FAT32 USB and APA Internal HDD users do NOT need to manually install the POPSTARTER folder to their memory card.**

The required files are handled differently for these methods.

### Other Methods

For the following methods, the **POPSTARTER** folder needs to be installed to your PS2 memory card:

* MX4SIO
* MMCE
* exFAT HDD (GPT/MBR)
* SMB

The folder can be found inside:

```text
Resources
└── Popstarter PS2 Drivers
    └── POPSTARTER
```

### Installation

1. Copy the entire **POPSTARTER** folder to your USB flash drive or memory card.
2. Launch **uLaunchELF** on your PlayStation 2.
3. Copy the `POPSTARTER` folder to:

```text
mc0:/
```

The final location should be:

```text
mc0:/POPSTARTER/
```

This only needs to be done once for each memory card.

> **Important:** FAT32 USB and APA Internal HDD users do not need to perform this memory-card installation step.

---

# Required Runtime Files

The required POPStarter runtime files are **copyrighted and will NOT be provided with this application**.

You must obtain them separately.

## USB / MX4SIO / MMCE / exFAT HDD (GPT/MBR) / SMB

For these methods, the required runtime files are:

```text
POPSTARTER.ELF
POPS_IOX.PAK
```

These files must be placed inside the `POPS` folder on your target storage device.

Example:

```text
POPS
├── POPSTARTER.ELF
├── POPS_IOX.PAK
└── YourGame.VCD
```

---

## APA Internal HDD

APA Internal HDD installations use different runtime files:

```text
POPS.ELF
POPS.PAK
IOPRP_252.IMG
```

These files are required by the APA HDD installation and must be supplied separately.

The application does **not** provide these copyrighted files.

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

The converter automatically scans all subfolders.

---

## Step 2 — Output Folder

Select where your converted **VCD** files should be saved.

For USB, MX4SIO, MMCE, exFAT HDD (GPT/MBR), and SMB installations, you can select the `POPS` folder on your target device.

Example:

```text
USB:\POPS
```

or:

```text
PS2SMB\POPS
```

For **APA Internal HDD**, follow the dedicated APA instructions below.

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

# 💾 USB / MX4SIO / MMCE / exFAT HDD (GPT/MBR)

Use this method when playing PS1 games from:

* USB Flash Drive
* MX4SIO
* MMCE
* exFAT HDD (GPT/MBR)

---

## Required Files

Copy the following copyrighted runtime files into the `POPS` folder on your storage device:

```text
POPSTARTER.ELF
POPS_IOX.PAK
```

These files are **not included** with the application.

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

Do **not** select the `POPS` folder itself.

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

Downloads available metadata files for supported PS1 games.

---

### Aspect Ratio

Applies available Aspect Ratio patches created by **Hugopocked**.

---

## Install

Click **Run**.

Once complete:

1. Safely remove your storage device.
2. Connect it to your PlayStation 2.
3. Enable the **APPS** page inside OPL Settings.
4. Launch your games using POPStarter.

---

## Download Missing ART / CFG

The **ART/CFG** buttons allow you to download missing artwork and CFG files after the initial installation.

This is useful if the download server was temporarily unavailable when you originally installed your games.

If some artwork or CFG files could not be downloaded, reconnect your storage device and use the corresponding **ART/CFG** button to download the missing files later.

There is no need to reconvert or reinstall the games.

---

# 🌐 SMB

Use this tab when storing your PlayStation 1 games on an SMB network share.

---

## Required Files

Copy the following copyrighted runtime files into your SMB `POPS` folder:

```text
POPSTARTER.ELF
POPS_IOX.PAK
```

These files are **not included** with the application.

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

Do **not** select the `POPS` folder itself.

---

## Edit POPS SMB Drivers

The SMB tab includes a built-in **Edit POPS SMB Drivers** button that allows you to configure the network settings used by POPStarter when loading PS1 games over SMB.

This tool edits two configuration files:

* **IPCONFIG.DAT** – PS2 network settings
* **SMBCONFIG.DAT** – SMB server settings

### How to Use

1. Click **Edit POPS SMB Drivers**.
2. A new window will open with two tabs:

   * **IPCONFIG.DAT** – Enter your PS2's IP address, Netmask, and Gateway.
   * **SMBCONFIG.DAT** – Enter your PC's IP address, SMB port, share name, username, and password.
3. Click **Restore Defaults** to reset all fields to their default values.
4. Click **Save** to write the changes to disk.
5. Follow the instructions shown by the application to deploy the updated POPSTARTER files to your memory card.

> **Note:** Leave the SMB Port field blank to use the default SMB port (445). Only specify a port if your SMB server is configured to use a different port.

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

Downloads available metadata files.

---

### Aspect Ratio

Applies available Aspect Ratio patches created by **Hugopocked**.

---

## Install

Click **Run**.

After completion:

1. Refresh your SMB share if necessary.
2. Launch Open PS2 Loader.
3. Enable the **APPS** page.
4. Launch your PS1 games.

---

## Download Missing ART / CFG

The **ART/CFG** buttons can be used to download missing artwork and CFG files after installation.

If the download server was unavailable during the initial installation, you can simply use the corresponding **ART/CFG** button later when the server becomes available.

There is no need to reconvert or reinstall your games.

---

# 💿 APA (Internal HDD)

Use this tab if you want to install your PlayStation 1 games directly onto an **APA-formatted internal PS2 HDD**.

Unlike USB, MX4SIO, MMCE, exFAT HDD (GPT/MBR), and SMB, games are first converted into VCD files on your PC and then transferred directly to the internal HDD.

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

### Using the Built-in Create POPS Partition Tool

1. Click **Transfer to HDD** in the APA tab.
2. Click **Connect** and select your PS2 HDD.
3. If no `__.POPS` partitions exist, you will see a warning.
4. Click **Create POPS Partition**.
5. Choose a partition size using the slider or numeric input.
6. Click **Create**.
7. The tool will create the partition and automatically format it as PFS.

Once created, the partition will appear in the list and is ready for transferring games.

---

# Step 2 — Prepare the APA Runtime Files

APA installations require these copyrighted runtime files:

```text
POPS.ELF
POPS.PAK
IOPRP_252.IMG
```

Place these files inside:

```text
Resources
└── APA HDD Binaries
```

The application will automatically detect the Resources folder supplied with the program.

> **Important:** These files are copyrighted and are **not included** with this application. They must be obtained separately.

These files only need to be transferred once unless the POPS partition is recreated.

---

# Step 3 — Create a Temporary Working Folder

For APA installations, create a **temporary working folder** anywhere on your PC.

Inside that folder, create a folder named:

```text
POPS
```

For example:

```text
D:\PS1_Conversion\
└── POPS
```

The `POPS` folder is where the converted VCD files will temporarily be stored before they are transferred to the internal HDD.

When using the **Game Converter** tab, select this temporary `POPS` folder as your **Output Folder**.

---

# Step 4 — Convert Your Games

Open the **Game Converter** tab.

Select:

* **Source Folder** → Your BIN/CUE or ZIP backups
* **Output Folder** → The temporary `POPS` folder you created

The application automatically detects its included `Resources` folder, so you do **not** need to manually select it.

Click:

* **Scan for Games**
* Select the games you want to convert
* **Convert Selected**

Once finished, your temporary `POPS` folder will contain the converted VCD files.

---

# Step 5 — Prepare the Installation

Open the **APA (Internal HDD)** tab.

Choose any desired options:

* Apply Cheats
* Apply HDTVFIX
* Download CFG / Metadata
* Aspect Ratio patches

Click **Run**.

---

# Step 6 — Transfer to the HDD

Click **Transfer to HDD**.

A new window will open.

1. Select your PlayStation 2 HDD from the drop-down list.
2. Click **Connect**.
3. Click **Transfer Binaries** if the APA runtime files have not already been installed.
4. Click **Start Transfer**.

The program will copy your converted games directly to the selected POPS partition.

If the required files have already been installed, the application will indicate that they are already installed.

---

# Additional APA Tools

## Download Missing ART

Downloads missing cover artwork for games already installed on the HDD.

---

## Download Missing CFG

Downloads missing CFG files for games already installed on the HDD.

---

## Create POPS Partition

Creates a new `__.POPS` partition on the HDD.

The tool automatically handles the required APA sub-partitioning and PFS formatting.

---

## Cleanup

The **Cleanup** button clears the temporary working `POPS` directory, making it easy to prepare for your next batch of conversions.

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

# 📥 Updating the Application

The application includes a built-in update system.

When a new version is released, the application can check the latest GitHub release and notify you when an update is available.

If you choose to update, the updater will:

1. Download the new application.
2. Verify the downloaded file using its SHA-256 checksum.
3. Replace the existing application.
4. Verify the installed file.
5. Launch the updated version automatically.

Your `Resources` folder and other files are not replaced by the updater.

> **Important:** Always keep the `Resources` folder in the same folder as the main application.

---

# Notes

* ZIP archives are extracted automatically during conversion.
* Multi-track games are merged automatically.
* Existing VCD files will not be overwritten unless **Overwrite Existing VCD Files** is enabled.
* The converter scans all subfolders recursively.
* Always keep a backup of your original PlayStation 1 games.
* APA partitions up to **128 GB** can be created directly from the GUI.
* SMB network settings can be edited directly from the application using the built-in **Edit POPS SMB Drivers** tool.
* Missing ART and CFG files can be downloaded later using the **ART/CFG** buttons.
* The application automatically detects the included `Resources` folder.
* Copyrighted POPStarter runtime files are **NOT provided** with this application.

---

# ❤️ Credits

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

Enjoy your PlayStation 1 library on the PlayStation 2!

**Happy Gaming! 🎮**
