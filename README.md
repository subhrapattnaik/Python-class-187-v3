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
