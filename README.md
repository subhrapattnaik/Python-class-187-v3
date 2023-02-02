# Python-class-187-v3

Last Class:

 the particle system in VR.
We made the fireworks using the spe-particles component.
--------------------------------------------------------------------------------------------------
revising all the concepts of AR 
Augmented Reality (AR) means adding digital objects/content over the real world. AR applications help to enhance the real world by adding virtual objects into it, which feel very real.

In simple terms, augmented reality is adding digital objects in the real world generally by using the smartphone's camera, but in virtual reality, the physical world is completely replaced by the virtual environment with the help of VR headset devices. 

In AR, the user continues to be in touch with the real world while interacting with the virtual world. Whereas in VR, the user gets isolated from the real world

We used the A-Frame framework to create Web Based Augmented Reality scenes.

A-Frame is a framework based on HTML & JavaScript. To work with AR, we have to use AR.js library that can help us to create augmented reality scenes.
This library is specially designed to make augmented reality applications. The first step to use it is adding the aframe-ar.js library.

The arjs component is attached to the scene to make an Augmented Reality scene. 
--------------------------------------------------------------------------------------------------
The marker is nothing but the starting point of the coordinate system in the physical world where the object can be displayed. This means wherever we will place the marker that will become the origin(0,0,0), that will be the starting point of the coordinate system.

Hiro and Kanji markers.

later for the tiger image we added animation-mixer.
--------------------------------------------------------------------------------------------------

Apart from the Hiro and Kanji markers, we also how barcode markers work. The detection information of these markers is stored in a matrix, the most popular being the 3X3 and 4X4 matrix markers. These markers have unique ID values assigned to them. How did we use them in the code?

To use these in code, we set 2 attributes in arjs of . These are : detectionMode and codeMatrixType. 

By scanning barcode markers, we were able to show atoms corresponding to them, and we also showed the formation of compounds.
--------------------------------------------------------------------------------------------------

Next, we also learned about creating pattern markers.

To create pattern markers, we can take an image and create the pattern marker of that using an AR.js marker creating tool.

We can upload the image on this tool and adjust the pattern ratio, image size, and background border color. Then we can download the marker (in .patt format) as well as the marker image. Then we place these in the assets folder of our project.

We used a custom marker to display a food item and its ingredients in AR.
--------------------------------------------------------------------------------------------------

Location-based AR is a type of markerless Augmented Reality. It doesn’t need special markers to identify the location of virtual objects. In this, we can use our location instead of markers to create markerless AR scenes. It relies on GPS and other technologies to identify a device’s location and position with high accuracy.

we use two components in  to place the 3D model at a particular location. 

1. gps-entity-place: When this component is attached in  tag, it will assign a position (latitude and longitude) on the Earth to that entity.
In this component, we can provide the latitude and longitude as values to this component in the string format: gps-entity-place="latitude: ; longitude: ".
While using it, we had taken the values of latitude and longitude from Google Maps.

2. look-at: This component makes sure the entity always points to the camera. We give the value of the look-at component as a gps-camera so that it always faces the camera.

At last, to enable location AR, we set  as a GPS camera. We use the gps-camera component for this, along with two attributes: minDistance and positionMinAccuracy.
---------------------------------------------------------------------------------------------------
We used location based AR to show the directions from source to destination coordinates.
Mapbox Direction API.

-------------------------------------------------------------------------------------------------------
Another type of markerless AR that we learned was related to face recognition. Let's try to recollect how the computer recognizes faces using this visual. 

Detecting a face requires a lot of algorithms to work together. But we can divide it into a few broad steps:

1. To read any image; first, we will need to capture the image using a Camera.
2. Then, we can apply a face detection algorithm to detect the face.
3. Then, we would need to detect facial features like eyes, lips, etc.
4. In the end, we will generate an Array of face objects with other data related to faces.


we  used some predefined libraries/APIs to get this final data.
------------------------------------------------------------------------------------------
We created our own face filter app using AR face recognition. We created this app (FRAPP) using React Native. 

We used the FaceDetector module developed by Expo to help detect faces from the camera. Once it detects the faces, it gives us a  lot of information about them. Additionally, we installed and imported the dependencies: expo-camera and expo-permissions

-----------------------------------------------------------------------------------------
We learned about one more interesting concept called Image Tracking.

Image tracking is a feature of AR that gives apps the ability to detect 2D images and render content over them to appear in the form of videos, sound, text, 3D animations, etc. Similar to how we showed content over a marker, we can tell the computer to identify an image (the image tracker).

We used an NFT converter to convert an image into a tracker. NFT stands for Natural Feature Tracking. This is a technology that helps to create image trackers.
--------------------------------------------------------------------------------------
et’s create your portfolio to show all your projects done in AR/VR. You will create pattern markers for each project and design a portfolio page.

There are three parts to creating your AR/VR portfolio: 
creating pattern markers for each of your projects,
generating a QR code that we can scan, and finally, 
designing the layout how you would like your portfolio to be seen. 

host our project on GitHub and get the link.
--------------------------------------------------
The next step will be to generate our QR code which we will be adding to our portfolio.

https://www.qr-code-generator.com/


For this, we will open the QR Generator link, paste the GitHub link of our hosted project over there, and then download the QR image.

We will then add it to our portfolio page and place it appropriately.

We should remember one thing that we need to place the pattern markers far away from each other in the portfolio to avoid overlapping of the image/video assigned to each marker.


