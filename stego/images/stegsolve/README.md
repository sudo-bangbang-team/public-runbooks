# Stegsolve

## Info

From the app:

> Stegsolve is a stegano solver for challenges. It provides these main functions:
> * A quick view of different bit planes and some simple transformations.
> * Data extraction from planes. This can be row order or column order, with bits treated as a bitstream and converted into bytes.
> * Some simple checking of file formats and reporting on the filesize, additional bytes, file holes, etc. This is highly dependent upon the type of image.
> * Stereogram solver - simply change the offset until the image becomes visible.
> * Frame browser for animated images. This should also work for viewing layers in multi-layered PNG files.
> * Image combiner to combine two images in a variety of ways and browse through the different combinations.
>
> Copy/Cut and paste is available from most text using CTRL-C to copy, CTRL-V to paste and CTRL-X for cut.
>
> If an image fails to load, for example because it is corrupt, then file analysis will still open the file that you just tried to view. It may, however, crash out before reporting the information that you want to know. This will work though on images where the PNG has corrupted CRC values for example.

## Install

```bash
#!/bin/bash -ex

wget http://www.caesum.com/handbook/Stegsolve.jar -O stegsolve.jar
chmod +x stegsolve.jar

# either:
sudo mv stegsolve.jar /usr/local/bin

# or, to a different folder on your PATH already:
mv stegsolve.jar /some/path/to/folder/on/path
```

## Usage

```bash
java -jar stegsolve.jar
```

Either drag+drop an image from local file browser to window to use, or select File -> Open manually.

Thumb right / left to navigate various planes in the image to attempt to look for easily revealed items hidden in one of the planes.

If there is no flag obvious in the planes visually, can also manually inspect the plane bits by going to Analyze -> Data Extract and toggling with the settings in that menu.

## Previous uses / writeups

1. B01lers Bootcamp 2020 [Zima Blue](https://barelycompetent.dev/post/ctfs/b01lers-bootcamp-2020-writeups#zima-blue).
2. Houseplant CTF 2020 [Neko Hero](https://barelycompetent.dev/post/ctfs/rtcp-2020-writeups/#neko-hero).
3. csiCTF 2020 [unseen](https://barelycompetent.dev/post/ctfs/csictf-2020-writeups/#unseen). 
4. UMDCTF 2020 [UMBC Cyber Defense - can it be breached?
](https://barelycompetent.dev/post/ctfs/umbc-dawgctf-2020-writeups/#umbc-cyber-defense---can-it-be-breached).
5. castor's CTF 2020 [Jigglypuff’s Song](https://barelycompetent.dev/post/ctfs/castors-2020-writeups/#jigglypuffs-song).
   * This one shows extracting data from the plane bits using **"Data Extract"**.
