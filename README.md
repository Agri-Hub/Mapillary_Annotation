# Mapillary_Annotation

This dataset contains annotated street-level images of crops. Using the API of the crowdsourcing platform Mapillary, we automatically download all available street-level images over the area and time window of interest. Then, each downloaded image is matched with the corresponding LPIS object(s) it illustrates. We annotate images that are taken either towards the windshield direction (Case 1) or the window direction (Case 2). We move the initial geo-location coordinates (lat1, lon1) to new coordinates (lat2, lon2) that are d = 10m away in the direction of angle θ. For Case 1, we set θ = compass angle+45o for the right half of the image and θ = compass angle−45o for left half. For Case 2 we set θ = compass angle. 

Concequntly, we use a No Reference Image Quality Assessment (NR-IQA) algorithm, namely BRISQUE, to remove bad quality images. 
