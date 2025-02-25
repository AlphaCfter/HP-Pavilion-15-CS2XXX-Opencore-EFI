<p align="center">
  <a href="https://github.com/acidanthera/OpenCorePkg">
    <img src="https://raw.githubusercontent.com/acidanthera/OpenCorePkg/master/Docs/Logos/OpenCore_with_text_Small.png" alt="logo" height="80">
  </a>
</p>

<p align="center">
  <strong>Opencore 1.0.3</strong>  
</p>
<br>

### **Sources**
This is a simplified guide from [Dortania](https://dortania.github.io/OpenCore-Install-Guide/) which is a complete guide for building the opencore bootloader.

### **🍎 Requirements**
- [BalenaEtcher](https://etcher.balena.io/#download-etcher)
- [Explorer++](https://explorerplusplus.com/download)
- [MiniPartionTool](https://www.partitionwizard.com/download.html)

### **🖊️ Prepration**
First you have to have a copy of the MacOS Bigsur. There are three ways to achieve it
1. Download official macOS bigsur from Apple. This is possible to users who have a macbook. Execute

    `softwareupdate --fetch-full-installer --full-installer-version 11.6`

    Then, flash the downloaded file over USB

    `sudo /Applications/Install\ macOS\ Big\ Sur.app/Contents/Resources/createinstallmedia --volume /Volumes/USB`
    
2. Download from GibMacOS [Repository](https://github.com/corpnewt/gibMacOS)

    Clone the repository via git

    `git clone https://github.com/corpnewt/gibMacOS.git`

    Change directory to the working directory

    `cd gibMacOS`

    Execute

    `gibMacOS.bat` for Windows / `gibMacOS.command` for Linux/MacOS

3. MacOS Oralia Prebuilt Image

    Download [BigSur](https://olarila.com/topic/20141-release-macos-big-sur-1161/) file from Olaria forms

    Restore or flash via `BalenaEtcher`


### 🧷 Mounting and Replacing the EFI Folder on a Bootable USB

After flashing the image to your USB, you need to replace the existing EFI folder with a custom one. However, Windows does not allow direct access to EFI partitions, as it considers them unsafe. To work around this limitation, follow these steps:

#### **🏴󠁧󠁲󠀶󠀹󠁿 Mount the EFI Partition**
1. Download and install [MiniTool Partition Wizard](https://www.partitionwizard.com/download.html).
2. Launch the tool and locate your bootable USB drive.
3. Identify the **EFI partition** and right-click on it.
4. Select **"Change Drive Letter"**, assign a drive letter of your choice, and apply the changes.

#### **💽 Access the EFI Partition**
1. Download and open **Explorer++** as an administrator.
2. Navigate to the drive letter you assigned to the EFI partition.
3. Delete the existing **EFI** folder from the USB.

#### **📄 Copy the New EFI Folder**
1. Download the EFI folder from [your repository] and extract it.
2. Using **Explorer++**, copy the extracted **EFI** folder to the EFI partition on the USB.

#### **✅ Final Step: Boot from USB**
Your USB is now ready with the new EFI configuration. You can proceed to boot your system using the modified USB.


