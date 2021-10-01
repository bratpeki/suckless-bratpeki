# My fork of Suckless' Simple Terminal

## Original README

```
st - simple terminal
--------------------
st is a simple terminal emulator for X which sucks less.

Requirements
------------
In order to build st you need the Xlib header files.

Installation
------------
Edit config.mk to match your local setup (st is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install st (if
necessary as root):

    make clean install

Running st
----------
If you did not install st with make clean install, you must compile
the st terminfo entry with the following command:

    tic -sx st.info

See the man page for additional details.

Credits
-------
Based on Aurélien APTEL <aurelien dot aptel at gmail dot com> bt source code.
```

## Changes to the original project

Changes include:
- Different colorscheme
- Patches applied: [scrollback](https://st.suckless.org/patches/scrollback/), [anysize](https://st.suckless.org/patches/anysize/), [delkey](https://st.suckless.org/patches/delkey/), [workingdir](https://st.suckless.org/patches/workingdir/)
- Keymaps index shrinked and keymaps in general reworked

## Keymaps

<b>Important: </b>Keep in mind that TermMod implies the following: ``#define TERMMOD (ControlMask|ShiftMask)``

| Mask    | Key    | Function                |
| ------- | ------ | ----------------------- |
| Shift   | PgUp   | Scroll up 1 line        |
| Shift   | PgDown | Scroll down 1 line      |
| TermMod | PgUp   | Scroll up 10 lines      |
| TermMod | PgDown | Scroll down 10 lines    |
| Shift   | ⬆️      | Increase font size by 1 |
| Shift   | ⬇️      | Decrease font size by 1 |
| TermMod | ⬆️      | Increase font size by 3 |
| TermMod | ⬇️      | Decrease font size by 3 |
| TermMod | Home   | Reset font size         |
| TermMod | C      | Copy to system cliboard |
| TermMod | V      | Copy to system cliboard |

# Dependencies

The project uses the following dependencies:

- `transset-df`, needed for making `st` transparent (defined in `x.c`'s `void run()` command)

