# File Magic Numbers

Magic numbers are the first bits of a file which uniquely identify the type of file. This makes programming easier because complicated file structures need not be searched in order to identify the file type.

For example, a JPEG file starts with `FF D8 FF E0 00 10 4A 46 49 46 00 01 01 01 00 47`. The `FF D8` shows that it's a JPEG file, and `FF E0` identifies a JFIF type structure. Although an ASCII encoding of "JFIF" follows after a length code, this is not necessary to identify the file. The first 4 bytes uniquely do that.

Below is an ongoing list of file-type magic numbers.

## Image Files

| File type                         | Typical extension | Hex digits            | ASCII digits     | Description            |
|------------------------------------|-------------------|-----------------------|------------------|------------------------|
| Bitmap format                      | .bmp              | 42 4D                 | BM               |                        |
| FITS format                        | .fits             | 53 49 4D 50 4C 45     | SIMPLE           |                        |
| GIF format                         | .gif              | 47 49 46 38           | GIF8             |                        |
| Graphics Kernel System             | .gks              | 47 4B 53 4D           | GKSM             |                        |
| IRIS rgb format                    | .rgb              | 01 DA                 | ..               |                        |
| ITC (CMU WM) format                | .itc              | F1 00 40 BB           | ....             |                        |
| JPEG File Interchange Format       | .jpg              | FF D8 FF E0           | ....             |                        |
| NIFF (Navy TIFF)                   | .nif              | 49 49 4E 31           | IIN1             |                        |
| PM format                          | .pm               | 56 49 45 57           | VIEW             |                        |
| PNG format                         | .png              | 89 50 4E 47           | .PNG             |                        |
| Postscript format                  | .ps/.eps          | 25 21                 | %!               |                        |
| Sun Rasterfile                     | .ras              | 59 A6 6A 95           | Y.j.             |                        |
| Targa format                       | .tga              | XX XX XX              | ...              |                        |
| TIFF format (Motorola - big endian)| .tif              | 4D 4D 00 2A           | MM.*             |                        |
| TIFF format (Intel - little endian)| .tif              | 49 49 2A 00           | II*.             |                        |
| X11 Bitmap format                  | .xbm              | XX XX                 |                  |                        |
| XCF Gimp file structure            | .xcf              | 67 69 6D 70 20 78 63 66 20 76 | gimp xcf |                        |
| Xfig format                        | .fig              | 23 46 49 47           | #FIG             |                        |
| XPM format                         | .xpm              | 2F 2A 20 58 50 4D 20 2A 2F | /* XPM */    |                        |

## Compressed Files

| File type   | Typical extension | Hex digits   | ASCII digits   | Description |
|-------------|-------------------|--------------|----------------|-------------|
| Bzip        | .bz               | 42 5A        | BZ             |             |
| Compress    | .Z                | 1F 9D        | ..             |             |
| gzip format | .gz               | 1F 8B        | ..             |             |
| pkzip format| .zip              | 50 4B 03 04  | PK..           |             |

## Archive Files

| File type      | Typical extension | Hex digits       | ASCII digits       | Description            |
|----------------|-------------------|------------------|--------------------|------------------------|
| TAR (pre-POSIX)| .tar              | XX XX            | (a filename)       |                        |
| TAR (POSIX)    | .tar              | 75 73 74 61 72   | ustar (offset by 257 bytes) |         |

## Executable Files

| File type                      | Typical extension | Hex digits            | ASCII digits           | Description |
|---------------------------------|-------------------|-----------------------|------------------------|-------------|
| MS-DOS, OS/2 or MS Windows      |                   | 4D 5A                 | MZ                     |             |
| Unix ELF                        |                   | 7F 45 4C 46           | .ELF                   |             |

## Miscellaneous Files

| File type               | Typical extension | Hex digits   | ASCII digits   | Description |
|-------------------------|-------------------|--------------|----------------|-------------|
| pgp public ring          |                   | 99 00        | ..             |             |
| pgp security ring        |                   | 95 01        | ..             |             |
| pgp security ring        |                   | 95 00        | ..             |             |
| pgp encrypted data       |                   | A6 00        | ¦.             |             |

---

This is a list of commonly used file magic numbers. For further reference, please consult online databases like [Wikipedia](https://en.wikipedia.org/wiki/List_of_file_signatures) for a more comprehensive list of file signatures.
