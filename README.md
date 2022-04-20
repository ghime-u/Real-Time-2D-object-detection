# Real-Time-2D-object-detection
The objective of the project was to develop real time 2-D object recognition system which can recognize a set of objects in a rotation, scale and translation invariant manner. This was achieved using the following steps: Image Thresholding: The frame from live video and image dataset were preprocessed to make highly saturated pixels darker to efficiently seperate them from white background and converting pixels with intensity > 120 in grayscale to black to create a binary image containing only the objects  Cleaning Up: Filled the holes by applying morphological filters like dilate, erode, shrinking by writing grassfire transform to fill the additional holes  Segmentation and feature computation: Segmented the image into major regions and computed features like centroids, HuMoments(0-7) and stored the values into a database (csv file). The user can select region to detect new object and store them into the database. The database acts like a training set(model)  Classification: The program now detects major region from live video feed and computes the centroids and HuMoments of the region. These features are now compared with the features stored in the database with the help of different distance metrics like Euclidean distance, mix-max normalization, etc. and the closest matching object is displayed on screen.   The program also computes the confusion matrix for each object detected