# Lab-5 - Face Clustering using K-Means

## Aim
The aim of this lab is to detect human faces from an image and group similar faces using a machine learning algorithm. We extract colour-based features (Hue and Saturation) from detected faces and apply K-Means clustering to divide faces into groups. A new face image is then classified based on the nearest cluster.

## Methodology
Following steps were performed:
1. Face Detection
  The input image was converted to grayscale.
  Haar Cascade Classifier (OpenCV) was used to detect faces.
  Rectangles were drawn around detected faces.

2. Feature Extraction
  The image was converted from BGR to HSV colour space.
  For each detected face:
    Mean Hue was calculated (represents colour).
    Mean Saturation was calculated (represents intensity).
  Each face was represented as a 2D feature point → (Hue, Saturation).

3. Clustering using K-Means
  K-Means clustering was applied with K = 2.
  Faces with similar colour characteristics were grouped together.
  Cluster centroids were calculated.

4. Template Face Classification
  A new face image (Dr. Shashi Tharoor) was detected.
  Hue and Saturation features were extracted.
  The trained K-Means model predicted which cluster the face belongs to.

5. Visualisation
  All faces were plotted in Hue vs Saturation space.
  Different clusters were shown in different colours.
  Cluster centroids were marked.
  The template face was plotted to show its predicted cluster.

## Key Findings
Faces were successfully detected using Haar Cascade.                
Hue and Saturation features provided a simple way to compare faces.              
K-Means clustering grouped faces based on colour similarity.                
The template image was correctly classified into the nearest cluster.              
Visualisation clearly showed separation between clusters.               

## Results & Visualisations
![Face Detection](Screenshot%202026-02-15%20170028.png)
![Clustering](output%201.png)
![Clustering with Centroids](output%202.png)
![Dr Detection](Screenshot%202026-02-15%20170106.png)
![Template Clustering](output%203.png)
![Final Clustering](output%204.png)

## Conlusion
In this lab, we implemented a simple face grouping and classification system using computer vision and machine learning techniques. Faces were detected using OpenCV, colour features were extracted using HSV colour space, and K-Means clustering grouped similar faces together. A new face image was successfully classified based on the trained model. This experiment demonstrated the practical use of feature extraction, clustering, and visualisation in image-based machine learning problems.

