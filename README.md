# text-extraction-using-open-cv-and-ocr
Opencv and Tesseract
Optical character recognition
OCR stands for Optical Character Recognition. It is a technology that recognizes text within a digital image. It is commonly used to recognize text in scanned documents and images. OCR software can be used to convert a physical paper document, or an image into an accessible electronic version with text.
Tesseract


Tesseract is an optical character recognition engine for various operating systems. It is free software, released under the Apache License. Originally developed by Hewlett-Packard as proprietary software in the 1980s, it was released as open source in 2005 and development has been sponsored by Google. for more details Tesseract.


Opencv



Opencv Open Source Computer Vision Library is an open source computer vision and machine learning software library. OpenCV was built to provide a common infrastructure for computer vision applications and to accelerate the use of machine perception in the commercial products. Being an Apache 2 licensed product, OpenCV makes it easy for businesses to utilize and modify the code.for more details opencv.
Installation
Follow the bellow steps for required packages

Clone the repositry
Create Virtul Environment and activate it
python -m venv venv
make sure you are in correct directory. in our case inside cloned repository folder
run this command to install required packages pip install -r .\requirements.txt, once installation success,
sudo apt install tesseract-ocr -y
sudo apt install tesseract-ocr-heb
sudo apt install tesseract-ocr-all -y for all languages, default language is English
run the file ocr_tesseract.py
Additional Setup for Windows
download the file exe from tesseract web or github .
Install the tesseract.exe and while installation copy the path
After done the installation, Open Environment varibales in Your PC.
Add Path (which is cpoied while installing)
Add variable TESSDATA_PREFIX=Your tesseract path\tessdata
In your code add this line and path of tesseract
pytesseract.pytesseract.tesseract_cmd = r"\tesseract.exe"

Note : That path must contain bin,tessdata folders

How it works
First we are opening an Image, which we have to convert
Then, finding boxes using opencv and draw the box with green indication around box, then we capture the bounding values x,y,height and width and save them into the variables.
Now, cropping the image with bounding values. X,Y values for start point and height, width values for draw the box.
send to pyTesseract, That's it and the output value or recognized text are stored at text variable
