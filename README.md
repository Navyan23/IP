# IP
**1.Develop a program to display a grayscale image using read and write operations**<br>
import cv2<br>
img=cv2.imread('img.jpg',0)<br>
cv2.imshow('image',img)<br>
cv2.waitKey(0)<br>
cv2.destroyAllWindows()<br>

**Output:**<br>
![image](https://user-images.githubusercontent.com/97940058/173810505-979b82e1-7cc9-4eb1-a8ff-50228060d653.png)<br>
*************************************************************************************************************************<br>

**2.Develop a program to display the image using mat plot lib**<br>
import matplotlib.image as mping<br>
import matplotlib.pyplot as plt<br>
img=mping.imread('img.jpg')<br>
plt.imshow(img)<br>

**Output:**<br>
![image](https://user-images.githubusercontent.com/97940058/173811930-e9e160ea-d325-4c99-a3dd-c41bdec26649.png)<br>


**3.Develop a program to perform a linear transformation**<br>
1)Rotation<br>
import cv2<br>
from PIL import Image<br>
img=Image.open('img.jpg')<br>
img=img.rotate(180)<br>
img.show()<br>
cv2.waitKey(0)<br>
cv2.destroyAllWindows()<br>

**Output:**<br>
![image](https://user-images.githubusercontent.com/97940058/173813674-1c4754cd-ea9c-4fa2-9ffe-ca23af66b9a1.png)<br>

**4.Develop a program to conver color tree to Rgb Color values**<br>
from PIL import ImageColor<br>
img1=ImageColor.getrgb("yellow")<br>
print(img1)<br>
img2=ImageColor.getrgb("red")<br>
print(img2)<br>

**Output:**<br>
![image](https://user-images.githubusercontent.com/97940058/173814321-0f9c723c-4bb6-4796-838a-55a29b425b5f.png)<br>

**5.Write a program to create image using a color**<br>
from PIL import Image<br>
img=Image.new('RGB',(200,400),(255,255,0))<br>
img.show()<br>

**Output:**<br>
![image](https://user-images.githubusercontent.com/97940058/173815086-5e10e1e1-ee52-4821-8b0a-11fec815e210.png)<br>

**6.Develop a program to visualize the image using various color spaces**<br>
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

**Output:**<br>
![image](https://user-images.githubusercontent.com/97940058/173815946-eeebaef7-d9c0-4996-9e92-a2a64dc4dff7.png)<br>
![image](https://user-images.githubusercontent.com/97940058/173816178-a933cf9a-cc69-4271-9ab1-ed68cab30ce8.png)<br>
![image](https://user-images.githubusercontent.com/97940058/173816334-0feca8d5-21b1-40cd-96ab-8df53f69b402.png)<br>

**7.Write a program to display the image attributes**<br>
image=Image.open('img.jpg')<br>
print("Filename:",image.filename)<br>
print("Format:",image.format)<br>
print("Mode:",image.mode)<br>
print("size:",image.size)<br>
print("width:",image.width)<br>
print("Height:",image.height)<br>
image.close()<br>
**Output:**<br>
![image](https://user-images.githubusercontent.com/97940058/173817125-c09ae608-7dfb-44de-b7c8-0871bed4dfb4.png)<br>

**8.Develop a program to conver the original image to gray scale and then to binary**<br>
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

**Output:**<br>
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


Develop a program to read an image using URL<br>
from skimage import io
import matplotlib.pyplot as plt<br>
url='https://images.unsplash.com/photo-1600703136783-bdb5ea365239?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8Mnx8cmVkJTIwZmxvd2VyfGVufDB8fDB8fA%3D%3D&w=1000&q=80'
image=io.imread(url)<br>
plt.imshow(image)<br>
plt.show()<br>

Output:<br>
![image](https://user-images.githubusercontent.com/97940058/175257948-78fe3194-63c7-46d2-8abe-56021d6bdd55.png)<br>


Develop a program to mask and blur the image<br>
import cv2<br>
import matplotlib.image as mpimg<br>
import matplotlib.pyplot as plt<br>
img=mpimg.imread('fish3.jpg')<br>
plt.imshow(img)<br>
plt.show()<br>
![image](https://user-images.githubusercontent.com/97940058/175258451-47042a07-df8d-423f-9c64-53364085e01d.png)<br>
hsv_img = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)<br>
light_orange=(1,190,200)<br>
dark_orange=(18,255,255)<br>
mask = cv2.inRange(hsv_img,light_orange,dark_orange)<br>
result=cv2.bitwise_and(img,img,mask=mask)<br>
plt.subplot(1,2,1)<br>
plt.imshow(mask,cmap="gray")<br>
plt.subplot(1,2,2)<br>
plt.imshow(result)<br>
plt.show()<br>
![image](https://user-images.githubusercontent.com/97940058/175258867-b502187c-a1d5-42a0-add0-80deee0abc36.png)<br>

light_white=(0,0,200)<br>
dark_white=(145,60,255)<br>
mask_white=cv2.inRange(hsv_img,light_white,dark_white)<br>
result_white=cv2.bitwise_and(img,img,mask=mask_white)<br>
plt.subplot(1,2,1)<br>
plt.imshow(mask_white,cmap="gray")<br>
plt.subplot(1,2,2)<br>
plt.imshow(result_white)<br>
plt.show()<br>
![image](https://user-images.githubusercontent.com/97940058/175259639-13742a6e-9402-438e-90b4-2e95cebeb4c7.png)<br>

final_mask=mask+mask_white<br>
final_result=cv2.bitwise_and(img,img,mask=final_mask)<br>
plt.subplot(1,2,1)<br>
plt.imshow(final_mask,cmap="gray")<br>
plt.subplot(1,2,2)<br>
plt.imshow(final_result)<br>
plt.show()<br>
![image](https://user-images.githubusercontent.com/97940058/175260406-b25e69de-7d0c-47d7-8be2-35cada0f27f5.png)<br>

blur=cv2.GaussianBlur(final_result,(7,7),0)<br>
plt.imshow(blur)<br>
plt.show()<br>

![image](https://user-images.githubusercontent.com/97940058/175264941-cadefad9-5027-4c46-974d-974f57b6544b.png)<br>


Develop a program to perform arithmatic operations on image<br>
import cv2<br>
import matplotlib.image as mpimg<br>
import matplotlib.pyplot as plt<br>
img1=cv2.imread('bt1.jpg')<br>
img2=cv2.imread('bt2.jpg')<br>
fimg1=img1+img2<br>
plt.imshow(fimg1)<br>
plt.show()<br>
cv2.imwrite('output.jpg',fimg1)<br>
fimg2=img1-img2<br>
plt.imshow(fimg2)<br>
plt.show()<br>
cv2.imwrite('output.jpg',fimg2)<br>
fimg3=img1*img2<br>
plt.imshow(fimg3)<br>
plt.show()<br>
cv2.imwrite('output.jpg',fimg3)<br>
fimg4=img1/img2<br>
plt.imshow(fimg4)<br>
plt.show()<br>
cv2.imwrite('output.jpg',fimg4)<br>

Output:<br>
![image](https://user-images.githubusercontent.com/97940058/175265590-6e672eee-add1-4dc5-ac31-16517d99af9a.png)<br>
![image](https://user-images.githubusercontent.com/97940058/175265795-70cde284-b2fa-4945-a8be-3b23e2e32a6a.png)<br>
![image](https://user-images.githubusercontent.com/97940058/175265974-c7462f8e-ebd8-44d7-8ca6-f811014e7087.png)<br>
![image](https://user-images.githubusercontent.com/97940058/175266209-6a6b6284-8e26-41ca-9cef-8e9cac66d696.png)



Develop a program to change the image to different color spaces<br>
import cv2 <br>
img=cv2.imread("D:\\flower1.jpg")<br>
gray=cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)<br>
hsv=cv2.cvtColor(img,cv2.COLOR_BGR2HSV)<br>
lab=cv2.cvtColor(img,cv2.COLOR_BGR2LAB)<br>
hls=cv2.cvtColor(img,cv2.COLOR_BGR2HLS)<br>
yuv=cv2.cvtColor(img,cv2.COLOR_BGR2YUV)<br>
cv2.imshow("GRAY image",gray)<br>
cv2.imshow("HSV image",hsv)<br>
cv2.imshow("LAB image",lab)<br>
cv2.imshow("HLS image",hls)<br>
cv2.imshow("YUV image",yuv)<br>
cv2.waitKey(0)<br>
cv2.destroyAllWindows()<br>

Output:<br>
![image](https://user-images.githubusercontent.com/97940058/175268656-a95b8986-4d80-4e17-a954-586270cc0ef0.png)<br>
![image](https://user-images.githubusercontent.com/97940058/175268891-acb27b76-a9b8-4959-a877-7a0d7d2544d2.png)<br>
![image](https://user-images.githubusercontent.com/97940058/175269107-99d9cd1d-7d4f-40d4-b632-164c273673e3.png)<br>
  ![image](https://user-images.githubusercontent.com/97940058/175269323-ef7282cd-2b28-4d3e-8413-658d17a0a3fe.png)<br>
  ![image](https://user-images.githubusercontent.com/97940058/175269542-10409f54-064b-496f-913d-115fad8d9113.png)<br>
  
  
Develop aprogram to create an image using 2D array<br>
import cv2 as c<br>
import numpy as np<br>
from PIL import Image<br>
array = np.zeros([100,200,3],dtype=np.uint8)<br>
array[:,:100]=[255,130,0]<br>
array[:,100:]=[0,0,255]<br>
img=Image.fromarray(array)<br>
img.save('image1.png')<br>
img.show()<br>
c.waitKey(0)<br>

Output:<br>
![image](https://user-images.githubusercontent.com/97940058/175272710-ca0aa707-9341-46d7-8149-d7e5da5e7317.png)

program to perform bitwise operations<br>
import cv2<br>
import matplotlib.pyplot as plt<br>
image1=cv2.imread('bt1.jpg')<br>
image2=cv2.imread('bt1.jpg')<br>
ax=plt.subplots(figsize=(15,10))<br>
bitwiseAnd=cv2.bitwise_and(image1,image2)<br>
bitwiseOr=cv2.bitwise_or(image1,image2)<br>
bitwiseXor=cv2.bitwise_xor(image1,image2)<br>
bitwiseNot_img1=cv2.bitwise_not(image1)<br>
bitwiseNot_img2=cv2.bitwise_not(image2)<br>
plt.subplot(151)<br>
plt.imshow(bitwiseAnd)<br>
plt.subplot(152)<br>
plt.imshow(bitwiseOr)<br>
plt.subplot(153)<br>
plt.imshow(bitwiseXor)<br>
plt.subplot(154)<br>
plt.imshow(bitwiseNot_img1)<br>
plt.subplot(155)<br>
plt.imshow(bitwiseNot_img2)<br>
cv2.waitKey(0)<br>

Output:<br>
![image](https://user-images.githubusercontent.com/97940058/176425094-2994cde7-8ec4-4290-94a6-1143328759ae.png)<br>


program to blurring image<br>
import cv2<br>
import numpy as np<br>
image=cv2.imread('dog.jpg')<br>
cv2.imshow('Original Image',image)<br>
cv2.waitKey(0)<br>
Gaussian =cv2.GaussianBlur(image,(7,7),0)<br>
cv2.imshow('Gaussian Blurring',Gaussian)<br>
cv2.waitKey(0)<br>
median=cv2.medianBlur(image,5)<br>
cv2.imshow('Median Blirring',median)<br>
cv2.waitKey(0)<br>
bilateral=cv2.bilateralFilter(image,9,75,75)<br>
cv2.imshow('Bilateral Blurring',bilateral)<br>
cv2.waitKey(0)<br>
cv2.destroyAllWindows()<br>
Output:<br>
![image](https://user-images.githubusercontent.com/97940058/176425809-04bfe8ad-5c35-495a-a801-56104ba305ec.png)<br>
![image](https://user-images.githubusercontent.com/97940058/176426027-a6383d2c-1a47-4a8b-bc5d-b0511f740464.png)<br>
![image](https://user-images.githubusercontent.com/97940058/176426238-efa3d1ad-fb27-4c81-883d-b5e7c7a7737b.png)<br>
![image](https://user-images.githubusercontent.com/97940058/176426400-8803e296-5610-4004-8124-2e157ff9fac4.png)<br>


program to perform image enhancement<br>
from PIL import Image<br>
from PIL import ImageEnhance<br>
image=Image.open('dog.jpg')<br>
image.show()<br>
enh_bri=ImageEnhance.Brightness(image)<br>
brightness=1.5<br>
image_brightened=enh_bri.enhance(brightness)<br>
image_brightened.show()<br>
enh_col=ImageEnhance.Color(image)<br>
color=1.5<br>
image_colored=enh_col.enhance(color)<br>
image_colored.show()<br>
enh_con=ImageEnhance.Contrast(image)<br>
contrast=1.5<br>
image_contrasted=enh_col.enhance(contrast)<br>
image_contrasted.show()<br>
enh_sha=ImageEnhance.Sharpness(image)<br>
sharpness=3.0<br>
image_sharped=enh_sha.enhance(sharpness)<br>
image_sharped.show()<br>















  






























 






