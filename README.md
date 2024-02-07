# Vehicle-Registration-Number-Detection

This project involves detecting vehicles and their license plates, followed by extracting the text from the license plates, which represents the registration number of the identified vehicles.

The process begins with the execution of "detect number plate.ipynb" to detect vehicles and subsequently their license plates. This module uses two YOLOv5 models: one for vehicle detection (a pre-trained YOLOv5s model) and another for license plate detection of the identified vehicle (a custom-trained YOLOv5s model). The [Sort](https://github.com/abewley/sort) module is utilized to track the identified vehicles. Following this, images of both the identified vehicle and its corresponding license plate are stored in separate folders named "Detected Car Frames" and "Detected Plate Frames," respectively.

Subsequently, the second script, "detect registration number.ipynb" is executed. It processes the license plate images from the "Detected Plate Frames" folder to recognize the text on them. The recognized text is then verified and formatted to adhere to the specified registration number format (USA in my case), resulting in the extraction of the vehicle's registration number. Further steps are carried out, culminating in the generation of an Excel file containing the registration numbers of each vehicle.

The YOLOv5s model utilized for detecting license plates on identified vehicles was custom trained on a dataset comprising 754 images. These images were specifically prepared to focus on a single class: license plate. The dataset preparation process was facilitated using RoboFlow.

To utilize the Sort module, it must be downloaded from [this repository](https://github.com/abewley/sort).
