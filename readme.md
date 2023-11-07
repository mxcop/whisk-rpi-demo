# Whisk for the RPi4

To get started you'll need linux *(WSL will also work on Windows)*

### Prerequisites

- [`whisk`] buildsystem.
- `arm-linux-gnueabihf-gcc` arm cross-compiler. (or aarch64) <br>
```sh
$ sudo apt-get install gcc-arm-linux-gnueabihf
```

[`whisk`]: https://github.com/mxcop/whisk

### Building

To build the project *(for the Pi)* simply run:
```sh
$ whisk build . arm-linux-32 # or aarch64-linux-64
```

You can also build the project for your own machine: *(as long as you're on x86 64 bit linux)*
```sh
$ whisk build

$ whisk run
```

### Debugging

For debugging you'll need `gdb`, if you don't have it yet.<br>
Install it (on Debian) using `sudo apt install gdb`.

You can debug the program locally in vscode using `F5`. *(don't forget to `whisk build` first)*

### Uploading

To upload your program to the Pi I recommend using `scp`.<br>
It is a command line tool for uploading files over `ssh`.

Example usage:
```sh
$ scp ./bin/whisk-rpi usr@127.0.0.1:/home/usr/Desktop
```

### Notes

Don't forget to `chmod +xwr ./whisk-rpi` on the Pi after uploading it.<br>
Otherwise you will get a `Permission denied` error when attempting to run it.

That's it, it's that simple, **have fun** programming! :D
