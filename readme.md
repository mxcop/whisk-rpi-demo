# Whisk for the RPi4

This example uses `C` however you can easily change it to use `C++` instead.<br>
To get started you'll need linux *(WSL will also work on Windows)*

### Prerequisites

- `whisk` buildsystem.
- `arm-linux-gnueabihf-gcc` arm cross-compiler.

### Building

To build the project *(for the Pi)* simply run:
```sh
$ whisk build . arm-linux-32
```

You can also build the project for your own machine: *(as long as you're on x86 64 bit linux)*
```sh
$ whisk build

$ whisk run
```

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
