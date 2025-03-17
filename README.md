# Strask Layout
A custom keyboard layout optimized for the Polish language.
![layout1](https://github.com/Nakeyan/Strask-layout/blob/main/img/1.jpg?raw=true)
![layout2](https://github.com/Nakeyan/Strask-layout/blob/main/img/2.jpg?raw=true)
![layout3](https://github.com/Nakeyan/Strask-layout/blob/main/img/3.jpg?raw=true)
![layout4](https://github.com/Nakeyan/Strask-layout/blob/main/img/4.jpg?raw=true)

## Installation Guide (Linux - X11)
*Wayland support coming soon!*

### Step 1: Download and Copy the Layout
1. Download the `pl.xkb_symbols` file from the `Linux` folder.
2. Open a terminal and run the following command to copy the layout to the correct directory:
   ```sh
   sudo cp pl.xkb_symbols ${XKB_CONFIG_ROOT:-/usr/share/X11/xkb}/symbols/pl
   ```

### Step 2: Modify the `evdev.xml` File
1. Open the `evdev.xml` file located in `/usr/share/X11/xkb/rules/` using a text editor with root permissions:
   ```sh
   sudo nano /usr/share/X11/xkb/rules/evdev.xml
   ```
2. Find the section for Polish keyboard layouts.
3. Add the following lines inside the `<variantList>` section under Polish:
   ```xml
   <variant>
     <configItem>
       <name>custom</name>
       <description>Polish (STRASK)</description>
     </configItem>
   </variant>
   ```
4. Save the file and exit the editor.

### Step 3: Apply the Changes
Run the following command to apply the new keyboard layout:
```sh
setxkbmap -layout pl -variant custom
```
or go to your settings if you have DE and add Layout named Polish (KSTRDP/Strask)

Your Strask layout should now be available and ready to use!

## Installation Guide (Windows 7 - 11) (Coming soon!!)

### Step 1: Download the Layout
1. Download the `strask.klc` file from the `Windows` folder.

### Step 2: Download the MSKLC 
1. Open the `https://www.microsoft.com/en-US/download/details.aspx?id=102134` page and click download and install it on your Windows Machine

### Step 3: Open MSKLC
1. Open MSKLC then go to the "File" and open `strask.klc` which you downloaded. 
2. After that you need go to "Project" and click `Build DLL and Setup Package`

### Step 3: Settings
1. Go to your settings and click Time and Language "Czas i język" and go to Language tab "Język"
2. Then click on Polish "Polski" and click Options "Opcje" you will see Keyboards "Klawiatury" and click Add keyboard "Dodaj klawiaturę" and find Polish (Strask) "Sometimes there is a bug and you need to reboot your PC to use Keyboard layout"

Your Strask layout should now be available and ready to use!
