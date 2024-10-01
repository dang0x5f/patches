# Simple Terminal Patches

[stdotsucklessdotorg](https://st.suckless.org/)

Preferred patches:
* 1-scrollback-ringbuffer-0.9.2.diff - efficient kbd scroll
* 2-scrollback-float-0.9.2.diff - add kbd granularity instead of scrolling entire pages
* 3-scrollback-mouse-0.9.2.diff - mouse scroll
* 4-scrollback-mouse-altscreen-20220127.diff - mouse scroll without shift
* alpha-focus-0.9.diff - transparency dependent on focus
* blinking-cursor.diff - self identifying
* dracula-0.8.5.diff - theme
* xclearwin.diff - redraw on bg change

Good order to compile in. **Read compiler messages**.

## Installation

clone repo:
```shell
git clone https://git.suckless.org/st
```

apply patches accordingly:
```shell
patch < patch.diff
```

1. Patch scroll patches in their numbered order; 1,2,3,4.

2. Edit config.h mshortcuts[] replacing .i value with .f values just like the shortcuts[] below. This change is needed for the mousescroll to work with the float patch.

3. Compile & Test.

4. Apply each of the rest of the patches one at a time, check for .rej files, fix blunders, rm config.h, compile and test.
