# Questions

## What's `stdint.h`?

stdint.h is standard input; a standard library in c that specifies exact width integer types with exac minimum and maximum values in the C99 standard library section 7.18.

## What's the point of using `uint8_t`, `uint32_t`, `int32_t`, and `uint16_t` in a program?

these new names make it easier to remember what the different primitives mean;
uint8_t represente a BYTE
uint32_t represents a DWORD
int32_t represents a LONG;
uint16_t represents a WORD


## How many bytes is a `BYTE`, a `DWORD`, a `LONG`, and a `WORD`, respectively?

BYTE = 1 byte

bit = ...1 bit...
nybble = 4 bits = 1/2 byte
byte = 8 bits = 2 nybbles
WORD = 2 bytes = 4 nybbles = 16 bits
DWORD = 2 WORDs = 4 bytes = 8 nybbles = 32 bits

A LONG is a 32-bit signed integer, in twos-complement format; required to be at least 32 bits, and may or may not be larger than a standard integer. A conforming program can assume that it can safely store values between −(231−1)[9] and 231−1,[10] but it may not assume that the range isn't larger


QWORD = 2 DWORDs = 4 WORDS = ..... = 64 bits

## What (in ASCII, decimal, or hexadecimal) must the first two bytes of any BMP file be? Leading bytes used to identify file formats (with high probability) are generally called "magic numbers."

0   WORD    bfType
2   DWORD   bfSize

## What's the difference between `bfSize` and `biSize`?

biSize is constant, info header = 40 bytes
bfSize is the size of the file header plus the bitmap info header, pixels and pdding.

bf.bfSize = bi.biSize + sizeof(BITMAPFILEHEADER) + sizeof(BITMAPINFOHEADER)

## What does it mean if `biHeight` is negative?

biHeight is the height of the bitmap in pixels. If the number is negative, the image is a top-down DIB wit the origin at the upper left corner. DIB is device independent bitmap.

## What field in `BITMAPINFOHEADER` specifies the BMP's color depth (i.e., bits per pixel)?

28  WORD    biBitCount  he number of bits per pixel, which is the color depth of the image

## Why might `fopen` return `NULL` in lines 24 and 32 of `copy.c`?

TODO
because there is no actual location in memory that fopen can point to or there is no output file.

## Why is the third argument to `fread` always `1` in our code?

fread size is always 1 because we are iterating over every pixel

## What value does line 63 of `copy.c` assign to `padding` if `bi.biWidth` is `3`?

I think this will be 1.

## What does `fseek` do?

allows you to change the location of the file pointer.

## What is `SEEK_CUR`?

is a constant of the handling function in c language. it moves the file pointer to a given location.
