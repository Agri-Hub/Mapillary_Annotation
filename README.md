# Mapillary_Annotation

Using the API of the crowdsourcing platform Mapillary, we automatically download all available street-level images over the area of interest in the Netherlands for the year of 2017. Then, each downloaded image is matched with the corresponding LPIS object(s) it illustrates. We annotate images that are taken either towards the windshield direction (Case 1) or the window direction (Case 2).

The dataset contatins:
- street level images from the Mapillary API. We have also used the BRISQUE algorithm for No Reference Image Qaulity Assessment (NR-IQA) of the images, in order to exclude the unsuitable ones.
<!-- 
#### Example of bad quality image, which is discarded. -->
#### Example of good quality image, which is included.
![StreetLevel](/images/StreetLevel.png)

- a csv file, which contains the polygons of 80 parcels coupled with an id. 
<!--  We move the initial geo-location coordinates (lat1, lon1) to new coordinates (lat2, lon2) that are d = 10m away in the direction of angle θ.  <br />
For Case 1, we set θ = compass angle + 45<sup>o</sup> for the right half of the image and θ = compass angle−45<sup>o</sup>  for left half. For Case 2 we set θ = compass angle. Consequntly, we use a No Reference Image Quality Assessment (NR-IQA) algorithm, namely BRISQUE, to remove bad quality images. 
 -->
