# IP
1.Develop a program to display a grayscale image using read and write operations<br>
import cv2<br>
img=cv2.imread('img.jpg',0)<br>
cv2.imshow('image',img)<br>
cv2.waitKey(0)<br>
cv2.destroyAllWindows()<br>

Output:<br>
![image](https://user-images.githubusercontent.com/97940058/173810505-979b82e1-7cc9-4eb1-a8ff-50228060d653.png)<br>

2.Develop a program to display the image using mat plot lib<br>
import matplotlib.image as mping<br>
import matplotlib.pyplot as plt<br>
img=mping.imread('img.jpg')<br>
plt.imshow(img)<br>

Output:<br>
![image](https://user-images.githubusercontent.com/97940058/173811930-e9e160ea-d325-4c99-a3dd-c41bdec26649.png)<br>



