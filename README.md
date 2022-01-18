# Mapillary_Annotation

Using the API of the crowdsourcing platform Mapillary, we automatically download all available street-level images over the area of interest in the Netherlands for the year of 2017. Then, each downloaded image is matched with the corresponding LPIS object(s) it illustrates. We annotate images that are taken either towards the windshield direction (Case 1) or the window direction (Case 2).

We move the initial geo-location coordinates `(lat1, lon1)` to new coordinates `(lat2, lon2)` that are `d = 10m` away in the direction of angle θ.

For Case 1, we set `θ = compass angle + 45` for the right half of the image and `θ = compass angle−45` for left half. 

For Case 2 we set `θ = compass angle`. 

Consequntly, we use a No Reference Image Quality Assessment (NR-IQA) algorithm, namely BRISQUE, to remove bad quality images. 

The dataset is available [here](https://zenodo.org/record/5846417). It contains:

- street level images from the Mapillary API.  We have also used the BRISQUE algorithm for No Reference Image Qaulity Assessment (NR-IQA) of the images, in order to exclude the unsuitable ones.
<!-- 
#### Example of bad quality image, which is discarded. -->
#### Example of good quality image
![StreetLevel](/images/StreetLevel.png)

- a csv file, which contains the polygons of 45581 parcels together with an id for each parcel, the corresponging image id and date of the capture, the direction of the image that capture each parcel as well as the label of the illustrated crop. Below is shown an example of this file.
 
![Info](/images/info.png)

#### Overall Statistics

| Label | Count [^1] |
| --- | --- | --- | --- |
| `Grassland` | 40220 | 
| `Maize` | 4783 | 
| `Potatos` | 297 | 
| `Winter Wheat` | 127 |
| `Sumer Barley` | 56 | 
| `Sugar Beet` | 36 | 
| `Rice` | 33 | 
| `Onions` | 29 | 
| **`Total`**[^2] | **45581** | 
