
Debian
====================
This directory contains files used to package baisyccoind/baisyccoin-qt
for Debian-based Linux systems. If you compile baisyccoind/baisyccoin-qt yourself, there are some useful files here.

## baisyccoin: URI support ##


baisyccoin-qt.desktop  (Gnome / Open Desktop)
To install:

	sudo desktop-file-install baisyccoin-qt.desktop
	sudo update-desktop-database

If you build yourself, you will either need to modify the paths in
the .desktop file or copy or symlink your baisyccoinqt binary to `/usr/bin`
and the `../../share/pixmaps/baisyccoin128.png` to `/usr/share/pixmaps`

baisyccoin-qt.protocol (KDE)

