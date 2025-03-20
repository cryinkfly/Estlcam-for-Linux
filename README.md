# Estlcam-for-Linux

<a href="https://www.estlcam.de/">Estlcam</a> is a software for creating G-codes for a quick and easy start with the CNC milling machine and can also be used as control software if you use the associated Estlcam controller. This CAM software is used for work preparation and can be used for CNC machines with up to 3 axes. For example, it can be used in combination with a STEPCRAFT-800 and a home-made Arduino controller with Estclam firmware on it.

---

<div id="estclam-project-screenshots" align="center">
<h2>🖼 Screenshots from this project:</h2>
<img src="https://user-images.githubusercontent.com/79079633/224741741-68e78f5f-8d74-46a7-9c51-b8725448d0d5.png" width="700px" height="350px">
</br>
<img src="https://user-images.githubusercontent.com/79079633/224741750-651bb355-ddae-47eb-bc6c-d96fb39201e5.png" width="200px" height="150px">
<img src="https://user-images.githubusercontent.com/79079633/224741762-ff191dda-a6d2-4ba6-a3ce-02a1e5301527.png" width="200px" height="150px">
<img src="https://user-images.githubusercontent.com/79079633/224741727-65e5ef04-d94d-4a88-bbbf-30991ab7c2cf.png" width="200px" height="150px">
</div>

---

<div id="fusion360-installation" align="center">
  <h2>⚙️ Getting Started</h2>
  🔹 Check if your <a href="https://github.com/cryinkfly/Autodesk-Fusion-360-for-Linux/tree/main/files/extras/network/etc">network settings</a> are correctly configured!<br>
  🔹 Follow these steps to set up Wine and Winetricks before continuing with the installation:

  <h3>Step 1: Install Wine and Winetricks</h3>
  For <strong>Linux Mint 22.x</strong>, you can install Wine and Winetricks by running the following commands in your terminal:
  <pre>
    sudo dpkg --add-architecture i386
    sudo mkdir -pm755 /etc/apt/keyrings
    wget -O - https://dl.winehq.org/wine-builds/winehq.key | sudo gpg --dearmor -o /etc/apt/keyrings/winehq-archive.key -
    sudo wget -NP /etc/apt/sources.list.d/ https://dl.winehq.org/wine-builds/ubuntu/dists/noble/winehq-noble.sources
    sudo apt update
    sudo apt install --install-recommends winehq-staging winetricks</pre>
  
  For other systems, please refer to the official Wine installation guide at: <a href="https://wiki.winehq.org/Download">WineHQ Download</a>.

  <h3>Step 2: Configure Wine and Install Estlcam</h3>
  Once Wine and Winetricks are installed, proceed with the following commands:

  <pre>
    WINEPREFIX="$HOME/wineprefixes/estclam" winetricks -q sandbox
    cd "$HOME/wineprefixes/estclam/drive_c/users/$USER/Downloads"
    wget "https://www.estlcam.de/downloads/Estlcam_64_12126.exe"
    WINEPREFIX="$HOME/wineprefixes/estclam" wine Estlcam_64_12126.exe
    exit</pre>
  
  <p><strong>Important:</strong> Make sure to download the latest version of Estlcam. The link to the latest version can be found on the <a href="https://www.estlcam.de">official Estlcam website.</a></p>
</div>



