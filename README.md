# Strask Layout
A custom keyboard layout optimized for the Polish language.

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
       <description>Polish (KSTRDP/Strask)</description>
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

---

Let me know if you need any additional refinements or if you want to add troubleshooting tips! 🚀

