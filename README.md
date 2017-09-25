                   
# 3D Fountain Modeling from Single Image

This paper was presented in where 'Bozkırda Yapay Öğrenme Yaz Okulu 2017'(BYOYO 2017) was orginized by Hacettepe University.

In this study, our motivation is building a system for reconstructing fountains from a single image and generating a 3D mesh model of the output.

## Project Steps

### 1. Object Detection:                                                                                                                  
Fountain detection process is implemented with Darknet Yolo which is a framework for detection and classification with Convolutional Neural Networks(CNNs) architecture from deep learning techniques.

### 2. Object Segmentation:                                                                                                               
The fountain object is segmented out from the background by using GrabCut technique.

### 3. Generation of 3D Model:                                                                                                            
The general pattern of the model is formed by giving approximate radius values from top to bottom according to the symmetrical structure of all the side surfaces of the fountain. These radius values are calculated using contours of the fountain image. Contours are extracted by flood filling the foreground object and applying an edge detection method. In order to remove high frequency noise from the extracted boundaries, the image is low-pass filtered before edge detection.

### 4. Texturing to 3D Model:                                                                                                             
After the generation of the 3D model of the fountain object, texture coordinates are calculated for every vertex of the model and the input image is used as the texture map to increase realism of the output.
