**Problem Statement **


The aim here is to extract the latitude and longitude of the boundaries for a particular area (State, District, Village) from an image of the same. The input image contains the outline of the map and edge detection along with segmentation algorithms that can be implemented to achieve this task. Extracted edges would normally be in RGB range values which would then require to be scaled to the actual coordinates. This can be accomplished by using the minimum and maximum values along the x and y directions of the map which would then be used to scale the detected values. The output list of coordinates is to be stored in a GEOJSON format which is a usual representation of geographical coordinates similar to the JSON format. In order to obtain good accuracy, the extracted values should be up to the 8th or 10th decimal place. 

**Steps for extracting coordinates from map image: **
1.	Create an algorithm to detect the edges (Outlines) of a map. You may use a few image manipulation techniques like sharpness and smoothness to enhance the edge values.
2.	Create a function to segment different areas from the step 1. For instance, from a map of a particular state we need to extract all the districts.
3.	Scale the values to the actual latitude and longitude ranges of the area. The output detected edges would either range between 0 and 1 or 0 and 255. You need to scale the values respectively so that they match the regions latitude and longitude values.
4.	The final values should be up to 8th to 10th decimal place for a good accuracy.

Following is a sample input map along with the detected edge for a particular area (Expected output of detected region) and a GEOJSON sample.  

![image](https://user-images.githubusercontent.com/80118978/173184690-0a621204-2325-4eed-ba40-4dab7eed38c0.png)

Figure 1: Sample Input Map for Himachal Pradesh 

![image](https://user-images.githubusercontent.com/80118978/173184705-e6a87731-e77b-41a3-9049-e9e6c37c83dc.png)
![image](https://user-images.githubusercontent.com/80118978/173184714-fe5865ec-2b22-4b43-9faf-1c230d93ba16.png)

Figure 2: Left to Right - Detected Outline for a region (In Blue), Output GEOJSON format Sample 
