# Questions

## What's `stdint.h`?

TODO

## What's the point of using `uint8_t`, `uint32_t`, `int32_t`, and `uint16_t` in a program?

TODO

## How many bytes is a `BYTE`, a `DWORD`, a `LONG`, and a `WORD`, respectively?

TODO

## What (in ASCII, decimal, or hexadecimal) must the first two bytes of any BMP file be? Leading bytes used to identify file formats (with high probability) are generally called "magic numbers."

TODO

## What's the difference between `bfSize` and `biSize`?

TODO
biSize is constant, info header = 40 bytes.
bfSize is the size of the file header plus the bitmap info header.

## What does it mean if `biHeight` is negative?

TODO

## What field in `BITMAPINFOHEADER` specifies the BMP's color depth (i.e., bits per pixel)?

TODO

## Why might `fopen` return `NULL` in lines 24 and 32 of `copy.c`?

TODO
because there is no actual location in memory that fopen can point to or there is no output file.

## Why is the third argument to `fread` always `1` in our code?

TODO

## What value does line 63 of `copy.c` assign to `padding` if `bi.biWidth` is `3`?

TODO

## What does `fseek` do?

TODO

## What is `SEEK_CUR`?

TODO
