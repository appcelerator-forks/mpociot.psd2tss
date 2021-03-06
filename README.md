# PSD2TSS

## Description

PSD2TSS is a Photoshop (CS4 and up) Script that converts a given PSD file into Titanium Alloy XML and TSS markup. 

PSD2TSS turns a structured PSD file like this:

![image](http://www.marcelpociot.de/psd2tss/psd2tss_1.jpg)


Into:

	<Alloy>
		<Window id="Window">
			<ImageView id="ImageView_2"></ImageView>
		</Window>
	</Alloy>


	#ImageView_2 {
		'width': '513,' 
		'height': '105', 
		'top': '58', 
		'left': '163', 
		'image': '/images/psd2tss-1.png'
	} 

	#Window {
		'width': '640,' 
		'height': '919', 
		'top': '0', 
		'left': '0'
	} 

## Prerequisites
* ImageMagick installed

## Usage
* Download the github project.

* Extract it to the Presets/Scripts folder of your Photoshop installation folder.

* Open the `psd2tss.jsx` file and edit the following lines:

	This should represent the location of the `json.jsx` file inside the "lib" folder.
	
		#include /Users/marcelpociot/json.jsx

	Locate your ImageMagick installation

		 var conf = {
    		// EDIT
		    magick: '/opt/ImageMagick/bin/convert'
		 }
* Restart Photoshop if it was already running
* Open the example PSD
* Go to File > Scripts and select psd2tss from the list

## Todo
* Autodetect ImageMagick
* Autoload json.jsx
* Implement more properties :)

## Author

**Marcel Pociot**  
web: http://www.marcelpociot.de  
email: m.pociot@gmail.com
twitter: @marcelpociot


## License

    Copyright (c) 2013 Marcel Pociot

    Permission is hereby granted, free of charge, to any person obtaining a copy
    of this software and associated documentation files (the "Software"), to deal
    in the Software without restriction, including without limitation the rights
    to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
    copies of the Software, and to permit persons to whom the Software is
    furnished to do so, subject to the following conditions:

    The above copyright notice and this permission notice shall be included in
    all copies or substantial portions of the Software.

    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
    IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
    FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
    AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
    LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
    OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
    THE SOFTWARE.