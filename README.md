# STEREO-ComputerVision
In task, implement stereo correspondence algorithm that uses feature based methods.

I developed my program in jupyter notebook.<br />
In my file, i included images, because i renamed them. And i included output
screenshot if you do not want to open .ipynb file. 

# Orb Keypoints:
1- Use imread(“imagename”) to load images.<br />
2- Get keypoints and destinations from getOrbCorrespondences( image ).<br />
This method calls cv2.ORB_create and ORB.compute to get keypoint kp
and destination des.<br />
3- Get matches from getMatches(destination, destination). These are
correspondences between two images. We will have a list ot matches.<br />
4- We will draw disparity from matches with drawDisparity( … ), and i will
explain it deeply in next chapter.<br />

# drawDisparity(kp1, kp2, matches, realDisparity):
This method draws the disparity map for our target images. We need two
keypoints from image 1 and image 2 to compare. Matches list help us to index
keypoint that matches.<br />
## Algorithm:<br />
---For each match,<br />
--------Take matching coordinates from each keypoint<br />
--------------Compare their Y coordinates, they should be equal<br />
--------------Draw a square for image to the point where they match, and scale<br />
--------------its color to according to distance between keypoints.<br />

![Ekran görüntüsü_20230102_171827](https://user-images.githubusercontent.com/61903795/210243422-bf89d64e-dc07-4b61-bb8c-745d5416884e.png)
![Ekran görüntüsü_20230102_171858](https://user-images.githubusercontent.com/61903795/210243501-2c9a9907-7cf3-4b20-9eb4-c6e552ca74d8.png)
![Ekran görüntüsü_20230102_171916](https://user-images.githubusercontent.com/61903795/210243539-1d599c6c-6680-4f8b-b8dc-c4bb50b3e2a9.png)

More matches gives us better
outputs. “Point clouds you wee in middle are my output, and bottom full
images are from “middlebury.com”
