# P-Touch under Linux

For general infos about the P-Touch printers, see: [P-Touch Printers](./P-Touch-Printers.md)

Brother doesn't support Linux for their P-Touch printers (at least not for the affordable printers I've looked at). However, they provide USB protocol descriptions on their US support website for some selected printers.

> :warning: **Warning:** If you plan to use a P-Touch printer under Linux, inform yourself before a purchase as not all models are supported equally well.

*Some remarks: I've collected the infos on this page in 2025. They may be wrong, incomplete or get outdated over time. Please raise a GitHub issue for corrections. The printed labels were created using "TZe compatible" tapes, the results with genuine Brother tapes may be different.*

*The following lists some enthusiasts projects, the list is probably incomplete ...*

---

### ptouch-print

Command line tool from Dominik Radermacher to create simple text graphics and print them.

* Project: https://dominic.familie-radermacher.ch/projekte/ptouch-print/
* git repo: https://git.familie-radermacher.ch/linux/ptouch-print.git/
* Nice usage description: https://github.com/HenrikBengtsson/brother-ptouch-label-printer-on-linux

Supported printers:
* List (search for ptdevs): https://git.familie-radermacher.ch/linux/ptouch-print.git/tree/src/libptouch.c
* PT-P300BT: No
* PT-P710BT: Yes

For Experiences, see: [ptouch-print](./P-Touch-Linux-ptouch-print.md)

Git repository last updated (2025.03): 4 months ago

---

### CUPS
P-Touch printer driver for CUPS (Common Unix Printing System - https://de.wikipedia.org/wiki/Common_Unix_Printing_System).

Project page & git repo: https://github.com/philpem/printer-driver-ptouch/tree/master

Supported printers:
* List: https://github.com/philpem/printer-driver-ptouch/tree/master/printer
* PT-P300BT: https://github.com/philpem/printer-driver-ptouch/blob/master/printer/Brother-PT-P300BT.xml
* PT-P710BT: https://github.com/philpem/printer-driver-ptouch/blob/master/printer/Brother-PT-P710BT.xml

Experiences:
* TODO: Haven't tried it yet

Git repository last updated (2025.03): **1 year ago**

---

### PT-P300BT

Command line tool for the PT-P300BT. Written in Pure Python.

Project page & git repo: https://github.com/Ircama/PT-P300BT

I couldn't easily find a list of supported printers, except for the obvious PT-P300BT.

Experiences:
* TODO: Haven't tried it yet

Git repository last updated (2025.03): 2 months ago

---

### Pytouch Cube

GUI label editor for Brother P-Touch. Python QT5 based.

Project page & git repo: https://github.com/piksel/pytouch-cube

I couldn't easily find a list of supported printers.

Experiences:
* TODO: Haven't tried it yet

Git repository last updated (2025.03): **2 years ago**
