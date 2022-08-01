# image-retrieval-system

## Project Short Description
This is a Computer Vision project meant to present a Python approach to implement an image retrieval system solution. This system is meant to find the most
similar images from a given database with a query image that contains different types of landmarks, for example, landscapes, buildings, statues, logos. In this solution,
for each query image, the system generates an output that contains the top 25 most similar images from the database. The system's performence is higher if it is able to
find images that contain the same landmark as in the query image.

### About the data
The database contains a total of 500 images split into 50 classes, resulting in having 10 images per class; for *validation* there are *50 query images* and
for *testing* there are *100 query images*:
- *data/database*: location for the database images (500 in total)
- *data/queries_validation*: location for the validation images (50 in total)
- *data/queries_test*: location for the testing images (100 in total)

**NOTE:** The images are named using this pattern *{class}_{imagenumber}*


### Concepts used in this implementation
The solution is based on:
* <b>Bag of Visual Words</b> using SIFT algorithm to convert the features extracted from the images to 128 dimension vectors
* <b>MiniBatch K-Means clustering</b> (used this version of K-Means for computational reasons) applied on the previous 
  obtained images' descriptors, where each descriptor has a cluster associated with it
* <b>TF-IDF</b> used for assigning weights to the visual words
* <b>Cosine Similarity</b> formula used to determine how similar an image from the database is with a given query image. For each query image, the system outputs
  the first *25 images* in the highest cosine similarity order
  
## Developing Tools
The solution consists of a *Python notebook* developed in *Google Colab* only.
