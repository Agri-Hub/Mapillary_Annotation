# Mapillary_Annotation

Using the API of the crowdsourcing platform Mapillary, we automatically download all available street-level images over the area of interest in the Netherlands for the year of 2017. Then, each downloaded image is matched with the corresponding LPIS object(s) it illustrates. We annotate images that are taken either towards the windshield direction (Case 1) or the window direction (Case 2).



<!--  We move the initial geo-location coordinates (lat1, lon1) to new coordinates (lat2, lon2) that are d = 10m away in the direction of angle θ.  <br />
For Case 1, we set θ = compass angle + 45<sup>o</sup> for the right half of the image and θ = compass angle−45<sup>o</sup>  for left half. For Case 2 we set θ = compass angle. Consequntly, we use a No Reference Image Quality Assessment (NR-IQA) algorithm, namely BRISQUE, to remove bad quality images. 
 -->
