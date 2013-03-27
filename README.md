IMinify
=======
Bash script for batch image reduction while maintaining the directory structure.
 
SYNOPSIS
--------

	iminify -i [INPUT DIRECORY] -o [OUTPUT DIRECOTRY] [OTHER OPTION]
 
OVERVIEW
--------
Program minify images and copy direcotry structure. For its functionali using ImageMagick (convert).
 
DESCRIPTION
-----------
Settings:
 * `-i`	Path for directory with source images.
 * `-o`	Path for directory for processed images.
 * `-q`	Quality of images in percent. Represented by integer from 0-100. Default value is 95.
 * `-t`	List of processed image formats. Represented by extendsion with delimiter "," without spaces. Necessary are extensions in all occurrences. Default value is "jpg,JPG".
 * `-d`	Option for show same debug information. Check is only present option without value. Default value is false.
 * `-s`	Size of output images. Represented by string "HEIGHTxWIDTH". Default value is "1024x768".
 * `-f`	Force option for output destination. Check is only present option without value. Default value is false. Useable in three cases:
	 1. Entered output destination is not exist. If is option entered, create directory.
	 2. Entered output destination is not directory. If is option entered, remove old destination and create directory.
	 3. Entered output destination is not empty directory. If is option entered, remove files in directory.
 * `-h`	Show help.

EXAMPLE
-------
Resize all JPG and PNG images in directory `~/Images` and copied to directory `~/Mini` with output quality `80`, image size `800x600`, debug information and force creating output directory.

	iminify -i ~/Images -o ~/Mini -q 80 -s "800x600" -t "jpg,JPG,png,PNG" -d -f

INSTALL
-------

	git clone https://github.com/romanmatyus/iminify.git
	cd iminify
	sudo chmod +x iminify
	sudo cp iminify /usr/bin/iminify

SEE ALSO
--------
ImageMagick
 
COPYRIGHT
---------
Copyright (C) 2013 Roman Mátyus <romanmatyus@gmail.com>

All rights reserved.

License BSD.