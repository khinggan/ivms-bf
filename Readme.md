iVMS-bf — The Webcam Bruteforcer
---

A simple webcam bruteforcer based on Hikvision SDK. WOW, much alpha, very bug, pls help.

__UPD: Currently abandoned, [rewritten in Go](//github.com/superhacker777/hikka)__


## Building

In most cases, you need this:

  $ make

This includes patched SDK lib so you don't get a lot of useless debug warnings in your STDERR. But if you want to use an original library for some reason, you should make it like this:

  $ make vanilla
  
It seems like there's no excessive logging in Windows library, BTW.


## Platform support

I only care about Linux support now, so there's no way of making it work on Windows. There's a big __LATER__ here.


## Usage

Command to start bruteforce in 265 threads with IPs list stored in file "ips_file":

    $ ivms-bf -t 265 -i ips_file

You could also pass an IP list as an argument, which is helpful when you want to check a short list of cameras:

    $ ivms-bf 192.168.0.1 ...

__Passwords__ must be stored in file called "passwords", the same for __logins__ and "logins" file. It'll be hardcoded for a while.


## TODO:

1. Get rid of __argp__ to make it crossplatform.
2. Refactor most of the code and make it somehow better. I don't really know C++, so…
3. I don't know anything about makefiles too. I certainly did something wrong and I need to make it right.
4. Add more useful functions and do something with output formatting.


## Bugs

There may be some broken output. I didn't really know that STDOUT isn't thread-safe. I'm not that smart, uh. I'm going to fix it laterrrrrrr.
