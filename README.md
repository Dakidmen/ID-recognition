# ID-recognition
-  Recognizes people whose photos have been sent to app.py 's webservice

-  pip install os, Flask, FlaskRestful, shutil, pathlib2, mmh3, requests, json, base64, opencv-contrib-python, pickle, numpy, statistics, PIL, sys
to train images you have to exit the webservice with CTRL+C in the terminal

-  .json file has to be a dictionary like    dict = {name: "teresa coco", image: <image in 64bits>}

-  copy paste in your editor to convert your image to 64bits:
 
with open("teresa.jpg", "rb") as imageFile:
    stri = base64.b64encode(imageFile.read())
    jason_data = json.dumps(stri)
file = open("teresain64bits.json","w")
file.write(str(stri))
file.close()

fh = open("imageToSave.jpg", "wb")
fh.write(stri.decode('base64'))
fh.close()


-   Create a folder named "src" in your project's directory and inside it one called "images"
