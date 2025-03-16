# Strask-layout
custom keyboard Layout for Polish language

# Tutorial for Linux (x11) "there will be for wayland sooner!"
Download layout from Linux folder and open terminal and type sudo cp pl.xkb_symbols ${XKB_CONFIG_ROOT:-/usr/share/X11/xkb}/symbols/pl

Add this line of code to /usr/share/X11/xkb/rules/evdev.xml under polish layout

        <variant>
          <configItem>
            <name>custom</name>
            <description>Polish (KSTRDP/Strask)</description>
          </configItem>
        </variant>
