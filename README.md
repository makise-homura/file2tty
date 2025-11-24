### Requirements

This tool is designed to be used on Heltec HT-HD01 dongles with OpenWRT 23.05.5.

Install `inotifywait` package prior to use it.

### Installation

Put the script into `/usr/libexec`, chmod it to `755`.

Edit `/etc/inittab`: modify the line starting with `ttyS0` as following:

```
ttyS0::respawn:/bin/sh /usr/libexec/file2tty
```

Reboot.

### Writing to console

Write a line of text to `/run/file2tty.in`.

It will appear on serial console as kernel log line.

### Reading from console

Last line read from serial console will appear in `/run/file2tty.out`.