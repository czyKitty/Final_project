k-means
Implementation of k-means algorithm, k-means with initialization (kmean_plus), k-means with bisection (biKmeans).
To use:
from kmeans import *
#kmeans
centers = kmeanstrain(dataset,k)
clusters = kmeansfwd(dataset,k,nData,centers)
#kmeans with initialization
centers = k_plus(dataset,k)
cluster = kmeansfwd(dataset,k,nData,centers)
#kmeans with bisection
result = biKmeans(dataset,k)

k-medoids
Implementation of k-medoid algorithm.
To use: 
from sklearn.metrics.pairwise import pairwise_distances
import kmedoids
kmedoids.kMedoids(pairwise_distances(dataset, metric='euclidean'), k)

seg.py
This program takes in the name of image file and the k value, the log file is set to none, and display is set to yes by default. It will calculate the MSE and time for each method with image file and print that to screen. It will generate log file based on the file name given by -l, and show the image segmentation if -d is set to yes. Because of the issue with computational space, k-medoid would only be tested when the number of pixels is less than 1000. 
To run: python3 seg.py <imageFile> <k> -l <logFile> -d <yes/no>

testTrials.py
This program would generate log file for given image with k from 2 to 20, each will be the average of 20 trials. It would only run with image that has less than 1000 pixels.
To run: python3 testTrials.py <imageFile>
The formate of log file would be:
time
<run time of k-means>
<run time of k-means with initialization>
<run time of k-means with bisection>
<run time of k-medoid>
MSE
<MSE of k-means>
<MSE of k-means with initialization>
<MSE of k-means with bisection>
<MSE of k-medoid>
