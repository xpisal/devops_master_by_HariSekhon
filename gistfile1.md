# top (the UNIX process inspector) cheat sheet

This is a list of the most helpful keyboard commands I use within top.

## The basics

`h` shows help on interactive commands. Also see the [top manual page](http://man7.org/linux/man-pages/man1/top.1.html)

`q` to quit the program.

## Navigating

`Up` and `Down` to scroll through processes one by one, or `PageUp` and `PageDown` for paged navigation. 

`Left` and `Right` to navigate horizontally through fields (in case you're displaying a bunch).

`Shift+c` will show an index of where you are in the process list (eg 30/300 when your cursor is on process 30 and there are 300).

## Sorting 

`Shift+p` sort processes by CPU usage

`Shift+m` sort processes by memory usage

`Shift+r` reverse sort order

Sort on any field: Press `f` to bring up the Field Management menu. Select the field to sort on, press `s` and then `Escape`.

## Searching

`Shift+l` search for a string and highlights all occurences

`o` add a filter to limit which processes are displayed. A filter takes the format `{field name}{comparator}{value}`. For example, to see only processes owned by my user, I would add a filter `USER=eric`.

`Ctrl+o` view active filters.

`=` clear all filters.

## Other stuff

`m` switches memory views between the list of metrics and graph view.

`k` kill a process

`d` set the refresh rate (in seconds)

`Shift+w` saves the settings you've configured while running top to a file (`.toprc`) so they persist next time you use it.

`Shift+e` toggle the scale of memory metrics (between kilobytes and megabytes etc.) in the system memory summary, and `e` toggles the scale of memory metrics in the process list. The default is kilobytes, I find megabytes a useful level.
