PiFace Control and Display Emulator
===================================

Installation
------------
`pifacecad-emulator` is in the Raspbian repositories. Install with:

    $ sudo apt-get update && sudo apt-get install python3-pifacecad-emulator

Development Notes
-----------------
Uses Python 3 because of Barrier in threading.

Run the build_ui.sh script to build the UI first (you only have to do this
whenever you make a change to the UI in designer-qt4)

    $ ./bin/build_ui.sh

Test with:

    $ python3 tests.py

Otherwise, use just like you would pifacecad:

    $ python3
    >>> import pifacecad_emulator
    >>> cad = pifacecad_emulator.PiFaceCAD()
    >>> cad.lcd.write("hello")
