# My Emacs Flatpak 

## New: Emacs 30.1 with ripgrep, fd, pandoc, and shellcheck

These four binaries satisfy Doom Emacs' recommendations. You will likely need to add `export EMACS='/usr/bin/flatpak run org.gnu.emacs'` to your shell configuration. You may choose to additionally install Nerd Fonts using your system's package manager.

## With Pure-GTK interface and native-comp (lisp on libGCCjit)

This is a pre-configured flatpak manifest to build an Emacs branch with libjanson, libgccjit, and dependencies.  
This uses the latest releases of all components, except for gcc, which has JIT fixes in-tree, and Emacs, which has the experimental code bringing everything together.

This simply glues everything together into a trackable package rather than installing to `/usr/local/`.

If you'd prefer traditional `./configure && make && make install`, all functionality is in the master branch on Savannah.

## Building

Based off the official documentation:  
[https://docs.flatpak.org/en/latest/first-build.html](https://docs.flatpak.org/en/latest/first-build.html)

1. `flatpak install org.gnome.Sdk` (might also want to install the relevant theme you prefer)
2. `flatpak-builder --force-clean --user --install build-dir org.gnu.emacs.json` - this will take some time.

Rebuilding is simply repeating step 2.
