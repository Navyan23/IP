# IP
1.Develop a program to display a grayscale image using read and write operations<br>
import cv2<br>
img=cv2.imread('img.jpg',0)<br>
cv2.imshow('image',img)<br>
cv2.waitKey(0)<br>
cv2.destroyAllWindows()<br>

Output:<br>
![image](https://user-images.githubusercontent.com/97940058/173810505-979b82e1-7cc9-4eb1-a8ff-50228060d653.png)<br>
*******************************************************************************************************************************************************************<br>

2.Develop a program to display the image using mat plot lib<br>
import matplotlib.image as mping<br>
import matplotlib.pyplot as plt<br>
img=mping.imread('img.jpg')<br>
plt.imshow(img)<br>

Output:<br>
![image](https://user-images.githubusercontent.com/97940058/173811930-e9e160ea-d325-4c99-a3dd-c41bdec26649.png)<br>


3.Develop a program to perform a linear transformation<br>
1)Rotation<br>
import cv2<br>
from PIL import Image<br>
img=Image.open('img.jpg')<br>
img=img.rotate(180)<br>
img.show()<br>
cv2.waitKey(0)<br>
cv2.destroyAllWindows()<br>

Output:<br>
![image](https://user-images.githubusercontent.com/97940058/173813674-1c4754cd-ea9c-4fa2-9ffe-ca23af66b9a1.png)<br>

4.Develop a program to conver color tree to Rgb Color values<br>
from PIL import ImageColor<br>
img1=ImageColor.getrgb("yellow")<br>
print(img1)<br>
img2=ImageColor.getrgb("red")<br>
print(img2)<br>

Output:<br>
![image](https://user-images.githubusercontent.com/97940058/173814321-0f9c723c-4bb6-4796-838a-55a29b425b5f.png)<br>

5.Write a program to create image using a color<br>
from PIL import Image<br>
img=Image.new('RGB',(200,400),(255,255,0))<br>
img.show()<br>

Output:<br>
![image](https://user-images.githubusercontent.com/97940058/173815086-5e10e1e1-ee52-4821-8b0a-11fec815e210.png)<br>

6.Develop a program to visualize the image using various color spaces<br>
import cv2<br>
import matplotlib.pyplot as plt<br>
import numpy as np<br>
img=cv2.imread('img.jpg')<br>
plt.imshow(img)<br>
plt.show()<br>
img=cv2.cvtColor(img,cv2.COLOR_RGB2BGR)<br>
plt.imshow(img)<br>
plt.show()<br>
img=cv2.cvtColor(img,cv2.COLOR_BGR2HSV)<br>
plt.imshow(img)<br>
plt.show()<br>

Output:<br>
![image](https://user-images.githubusercontent.com/97940058/173815946-eeebaef7-d9c0-4996-9e92-a2a64dc4dff7.png)<br>
![image](https://user-images.githubusercontent.com/97940058/173816178-a933cf9a-cc69-4271-9ab1-ed68cab30ce8.png)<br>
![image](https://user-images.githubusercontent.com/97940058/173816334-0feca8d5-21b1-40cd-96ab-8df53f69b402.png)<br>

7.Write a program to display the image attributes<br>
image=Image.open('img.jpg')<br>
print("Filename:",image.filename)<br>
print("Format:",image.format)<br>
print("Mode:",image.mode)<br>
print("size:",image.size)<br>
print("width:",image.width)<br>
print("Height:",image.height)<br>
image.close()<br>
Output:<br>
![image](https://user-images.githubusercontent.com/97940058/173817125-c09ae608-7dfb-44de-b7c8-0871bed4dfb4.png)<br>

8.Develop a program to conver the original image to gray scale and then to binary<br>
import cv2<br>
#read the image file<br>
img=cv2.imread('flower4.jpg')<br>
cv2.imshow("RGB",img)<br>
cv2.waitKey(0)<br>
#GrayScale<br>
imgs=cv2.imread('flower4.jpg',0)<br>
cv2.imshow("Gray",imgs)<br>
cv2.waitKey(0)<br>
#Binary image<br>
ret,bw_img=cv2.threshold(imgs,127,255,cv2.THRESH_BINARY)<br>
cv2.imshow("Binary",bw_img)<br>
cv2.waitKey(0)<br>
cv2.destroyAllWindows()<br>

Output:<br>
![image](https://user-images.githubusercontent.com/97940058/174053716-8938d4f5-eae9-42ee-b9ba-fed2ff2e0c48.png)<br>
![image](https://user-images.githubusercontent.com/97940058/174054021-d5c718d0-f813-4472-9e71-9f06defce688.png)<br>
![image](https://user-images.githubusercontent.com/97940058/174054281-cc6fb558-c42b-4424-b5e5-d54cbdcdd461.png)<br>

9.Resize the original image<br>
import cv2<br>
img=cv2.imread('dog.jpg')<br>
print('original image length width',img.shape)<br>
cv2.imshow('original image',img)<br>
cv2.waitKey(0)<br>
imgresize=cv2.resize(img,(150,100))<br>
cv2.imshow('resized image',imgresize)<br>
print('Resized image length width',imgresize.shape)<br>
cv2.waitKey(0)<br>

Output:<br>
![image](https://user-images.githubusercontent.com/97940058/174055275-1d74a30b-86e0-433b-8423-b82576d97cce.png)<br>
![image](https://user-images.githubusercontent.com/97940058/174054877-d34d8d27-70f1-48d4-a8bb-015732738a12.png)<br>
![image](https://user-images.githubusercontent.com/97940058/174055030-d31691c0-2d5a-47f4-ad35-0a61a9f54641.png)<br>





















