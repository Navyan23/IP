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

**9.Resize the original image**<br>
import cv2<br>
img=cv2.imread('dog.jpg')<br>
print('original image length width',img.shape)<br>
cv2.imshow('original image',img)<br>
cv2.waitKey(0)<br>
imgresize=cv2.resize(img,(150,100))<br>
cv2.imshow('resized image',imgresize)<br>
print('Resized image length width',imgresize.shape)<br>
cv2.waitKey(0)<br>

**Output:**<br>
![image](https://user-images.githubusercontent.com/97940058/174055275-1d74a30b-86e0-433b-8423-b82576d97cce.png)<br>
![image](https://user-images.githubusercontent.com/97940058/174054877-d34d8d27-70f1-48d4-a8bb-015732738a12.png)<br>
![image](https://user-images.githubusercontent.com/97940058/174055030-d31691c0-2d5a-47f4-ad35-0a61a9f54641.png)<br>


**Develop a program to read an image using URL**<br>
from skimage import io
import matplotlib.pyplot as plt<br>
url='https://images.unsplash.com/photo-1600703136783-bdb5ea365239?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8Mnx8cmVkJTIwZmxvd2VyfGVufDB8fDB8fA%3D%3D&w=1000&q=80'
image=io.imread(url)<br>
plt.imshow(image)<br>
plt.show()<br>

**Output:**<br>
![image](https://user-images.githubusercontent.com/97940058/175257948-78fe3194-63c7-46d2-8abe-56021d6bdd55.png)<br>


**Develop a program to mask and blur the image**<br>
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


**Develop a program to perform arithmatic operations on image**<br>
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

**Output:**<br>
![image](https://user-images.githubusercontent.com/97940058/175265590-6e672eee-add1-4dc5-ac31-16517d99af9a.png)<br>
![image](https://user-images.githubusercontent.com/97940058/175265795-70cde284-b2fa-4945-a8be-3b23e2e32a6a.png)<br>
![image](https://user-images.githubusercontent.com/97940058/175266209-6a6b6284-8e26-41ca-9cef-8e9cac66d696.png)<br>



**Develop a program to change the image to different color spaces**<br>
import cv2 <br>
img=cv2.imread("D:\\rabbit.jpg")<br>
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

**Output:**<br>
![image](https://user-images.githubusercontent.com/97940058/178971202-4532cd3c-1431-4756-bb1d-5406d28083ae.png)<br>
![image](https://user-images.githubusercontent.com/97940058/178971350-0e8833af-5d3a-499a-821f-fff4003dcb0d.png)<br>
![image](https://user-images.githubusercontent.com/97940058/178971419-65af4d97-c409-467e-9989-22dbdfc1674d.png)<br>
![image](https://user-images.githubusercontent.com/97940058/178971484-648da2f1-97d4-446a-8a07-c099b9b81f74.png)<br>
![image](https://user-images.githubusercontent.com/97940058/178971550-43998073-179f-460c-8159-96aee1d176cc.png)<br>


**Develop a program to create an image using 2D array**<br>
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

**Output:**<br>
![image](https://user-images.githubusercontent.com/97940058/175272710-ca0aa707-9341-46d7-8149-d7e5da5e7317.png)

**program to perform bitwise operations**<br>
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

**Output:**<br>
![image](https://user-images.githubusercontent.com/97940058/176425094-2994cde7-8ec4-4290-94a6-1143328759ae.png)<br>


**program to blurring image**<br>
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
**Output:**<br>
![image](https://user-images.githubusercontent.com/97940058/178706561-5ac5f6a7-f574-43c6-b25a-5152fe537b54.png)<br>
![image](https://user-images.githubusercontent.com/97940058/178706697-e044098b-ff96-4ba9-80be-68919d2e101c.png)<br>
![image](https://user-images.githubusercontent.com/97940058/178706781-6292ee5b-6289-4f35-afa2-eea21a2baa7f.png)<br>
![image](https://user-images.githubusercontent.com/97940058/178706969-307a0887-0103-4255-89c0-30d68e448fc8.png)<br>



**program to perform image enhancement**<br>
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
**Output:**<br>
![image](https://user-images.githubusercontent.com/97940058/178445519-a854bb7e-8412-40a3-88bd-63aba67ef750.png)<br>
![image](https://user-images.githubusercontent.com/97940058/178445728-0374acda-2bf4-444c-b1c3-2ba3c58da177.png)<br>
![image](https://user-images.githubusercontent.com/97940058/178445887-e0de7f18-4abe-42e0-8acb-bf1254167f7e.png)<br>
![image](https://user-images.githubusercontent.com/97940058/178446106-7ed25d5d-d485-42f6-9526-0f593b4a4d45.png)<br>
![image](https://user-images.githubusercontent.com/97940058/178446453-4c487004-1861-4d1a-99c4-54569c7fd6e6.png)<br>


**program to perform morphological operations**<br>
import cv2<br>
import numpy as np<br>
from matplotlib import pyplot as plt<br>
from PIL import Image,ImageEnhance<br>
img=cv2.imread('dog.jpg',0)<br>
ax=plt.subplots(figsize=(20,10))<br>
kernel=np.ones((5,5),np.uint8)<br>
opening=cv2.morphologyEx(img,cv2.MORPH_OPEN,kernel)<br>
closing=cv2.morphologyEx(img,cv2.MORPH_CLOSE,kernel)<br>
erosion=cv2.erode(img,kernel,iterations=1)<br>
dilation=cv2.dilate(img,kernel,iterations=1)<br>
gradient=cv2.morphologyEx(img,cv2.MORPH_GRADIENT,kernel)<br>
plt.subplot(151)<br>
plt.imshow(opening)<br>
plt.subplot(152)<br>
plt.imshow(closing)<br>
plt.subplot(153)<br>
plt.imshow(erosion)<br>
plt.subplot(154)<br>
plt.imshow(dilation)<br>
plt.subplot(155)<br>
plt.imshow(gradient)<br>
cv2.waitKey(0)<br>

**Output:**<br>
![image](https://user-images.githubusercontent.com/97940058/178446928-de4ebaff-b721-443c-85ed-075ba963f80c.png)<br>


**Program to perform (i)  Read the image,convert it into grayscale image**<br>
                   **(ii) write(save) the grayscale image and**<br>
                   **(iii)dispaly the original image and grayscale image**<br>

import cv2<br>
OriginalImg=cv2.imread('f1.jpg')<br>
GrayImg=cv2.imread('f1.jpg',0)<br>
isSaved=cv2.imwrite('D:/i.jpg',GrayImg)<br>
cv2.imshow('Display Original Image',OriginalImg)<br>
cv2.imshow('Display Grayscale Image',GrayImg)<br>
cv2.waitKey(0)<br>
cv2.destroyAllWindows()<br>
if isSaved:<br>
    print('The image is successfully saved.')<br>
        
**Output:**<br>
![image](https://user-images.githubusercontent.com/97940058/178708657-b6e1ea9c-09c7-48d0-85c3-af43acc0626a.png)<br>
![image](https://user-images.githubusercontent.com/97940058/178708836-99bcb3d1-1830-454b-9bbb-967111b48504.png)<br>


**Program to perform slicing with background**<br>
import cv2<br>
import numpy as np<br>
from matplotlib import pyplot as plt<br>
image=cv2.imread('n1.jpg',0)<br>
x,y=image.shape<br>
z=np.zeros((x,y))<br>
for i in range(0,x):<br>
    for j in range(0,y):<br>
        if(image[i][j]>50 and image[i][j]<150):<br>
            z[i][j]=255<br>
        else:<br>
            z[i][j]=image[i][j]<br>
equ=np.hstack((image,z))<br>
plt.title('Graylevel slicing with background')<br>
plt.imshow(equ,'gray')<br>
plt.show()<br>

**Output:**<br>
![image](https://user-images.githubusercontent.com/97940058/178709561-d22a09a9-f523-45b5-8a94-faadb435767d.png)<br>



**Program to perform slicing without background**<br>
import cv2<br>
import numpy as np<br>
from matplotlib import pyplot as plt<br>
image=cv2.imread('n1.jpg',0)<br>
x,y=image.shape<br>
z=np.zeros((x,y))<br>
for i in range(0,x):<br>
    for j in range(0,y):<br>
        if(image[i][j]>50 and image[i][j]<150):<br>
            z[i][j]=255<br>
        else:<br>
            z[i][j]=0<br>
equ=np.hstack((image,z))<br>
plt.title('Graylevel slicing w/o background')<br>
plt.imshow(equ,'gray')<br>
plt.show()<br>

**Output:**<br>
![image](https://user-images.githubusercontent.com/97940058/178710061-76dc9488-20f6-4704-a406-9494f26dbe86.png)



**Develop a program to analize the image data using histogram with opencv**<br>

import cv2<br>
from matplotlib import pyplot as plt<br>
img = cv2.imread('dog.jpg',0)<br>
plt.hist(img.ravel(),256,[0,256])<br>
plt.show()<br>
**Output:**<br>
![image](https://user-images.githubusercontent.com/97940058/178958471-7b9a75a4-921c-458a-91f9-eb40d4f6ce09.png)<br>

**Develop a program to analize the image data using histogram with matplotlib**<br>
#importing required libraries of opencv<br>
import cv2<br>

#importing library for plotting<br>
from matplotlib import pyplot as plt<br>
 
#reads an input image<br>
img = cv2.imread('f1.jpg',0)<br>
 
#find frequency of pixels in range 0-255<br>
histr = cv2.calcHist([img],[0],None,[256],[0,256])<br>
 
#show the plotting graph of an image<br>
plt.plot(histr)<br>
plt.show()<br>

**Output:**<br>
![image](https://user-images.githubusercontent.com/97940058/178958920-fd6f8a51-8a43-4fda-b8ab-cf95507e5962.png)<br>

**Develop a program to analize the image data using histogram with  skimage**<br>
from skimage import io<br>
import matplotlib.pyplot as plt<br>
image = io.imread('dog.jpg')<br>

_ = plt.hist(image.ravel(), bins = 256, color = 'orange', )<br>
_ = plt.hist(image[:, :, 0].ravel(), bins = 256, color = 'red', alpha = 0.5)<br>
_ = plt.hist(image[:, :, 1].ravel(), bins = 256, color = 'Green', alpha = 0.5)<br>
_ = plt.hist(image[:, :, 2].ravel(), bins = 256, color = 'Blue', alpha = 0.5)<br>
_ = plt.xlabel('Intensity Value')<br>
_ = plt.ylabel('Count')<br>
_ = plt.legend(['Total', 'Red_Channel', 'Green_Channel', 'Blue_Channel'])<br>
plt.show()<br>
**Output:**<br>
![image](https://user-images.githubusercontent.com/97940058/178959675-1d2d142c-1c48-4bbd-a255-6a30dff507e5.png)<br>

**Develop a program to analize the image data using histogram with  numpy(1)**<br>
import cv2<br>
import numpy as np<br>
img=cv2.imread('dog.jpg')<br>
hist=cv2.calcHist([img],[0],None,[256],[0,256])<br>
plt.hist(img.ravel(),256,[0,256])<br>
plt.show()<br>
**output:**<br>
![image](https://user-images.githubusercontent.com/97940058/178960477-2e3f5d15-af76-48ae-95b5-931be5e26adc.png)<br>


**Develop a program to analize the image data using histogram with numpy(2)**<br>
import numpy as np<br>
import cv2 as cv<br>
from matplotlib import pyplot as plt<br>
img = cv.imread('dog.jpg')<br>
plt.imshow(img)<br>
plt.show()<br>
img = cv.imread('dog.jpg',0)<br>
plt.hist(img.ravel(),256,[0,256]);<br>
plt.show()<br>
**Output:**<br>
![image](https://user-images.githubusercontent.com/97940058/178960848-1c9e871d-1f7e-4bef-bcb1-6daefd2a088b.png)<br>
**************************************************************************************************************************

**program to perform basic image data analysis using intesity transformation:<br>
a)image negative<br>
b)log transformation<br>
c)gamma correction**<br>
%matplotlib inline<br>
import imageio<br>
import matplotlib.pyplot as plt<br>
import warnings<br>
import matplotlib.cbook<br>
warnings.filterwarnings("ignore",category=matplotlib.cbook.mplDeprecation)<br>
pic=imageio.imread('btf.jpg')<br>
plt.figure(figsize=(6,6))<br>
plt.imshow(pic)<br>
plt.axis('off')<br>

**Output**<br>
![image](https://user-images.githubusercontent.com/97940058/179957589-e3a94f5f-5b16-4d94-8de8-8badedb8cf48.png)<br>

negative=255- pic # neg = (L-1) - img<br>
plt.figure(figsize= (6,6))<br>
plt.imshow(negative);<br>
plt.axis('off');<br>
**Output:**<br>
![image](https://user-images.githubusercontent.com/97940058/179957946-cfc458e2-7f65-4aee-820a-bc9292adab7c.png)<br>

%matplotlib inline<br>
import imageio<br>
import numpy as np<br>
import matplotlib.pyplot as plt<br>
pic=imageio.imread('btf.jpg')<br>
gray=lambda rgb : np.dot(rgb[...,:3],[0.299,0.587,0.114])<br>
gray=gray(pic)<br>
max_=np.max(gray)<br>
def log_transform():<br>
    return(255/np.log(1+max_))*np.log(1+gray)<br>
plt.figure(figsize=(5,5))<br>
plt.imshow(log_transform(),cmap=plt.get_cmap(name='gray'))<br>
plt.axis('off');<br>
**Output:**
![image](https://user-images.githubusercontent.com/97940058/179958256-d16c4d31-b5b4-48d6-bf51-3b70a96a3afb.png)<br>

import imageio<br>
import matplotlib.pyplot as plt<br>
#Gamma encoding<br>
pic=imageio.imread('btf.jpg')<br>
gamma=2.2# Gamma < 1 ~ Dark ; Gamma > 1 ~ Bright<br>
gamma_correction=((pic/255)**(1/gamma))<br>
plt.figure(figsize=(5,5))<br>
plt.imshow(gamma_correction)<br>
plt.axis('off')<br>
**Output:**
![image](https://user-images.githubusercontent.com/97940058/179958458-5be03405-4967-45a9-82c7-001f5f74279a.png)<br>

**program to perform basic imafe manipulations:<br>
a)Sharpness<br>
b)Flipping<br>
c)cropping**<br>
#Image sharpen<br>
from PIL import Image<br>
from PIL import ImageFilter<br>
import matplotlib.pyplot as plt<br>
#Load the image<br>
my_image = Image.open('lion.jpg')<br>
#use shrpaen function<br>
sharp = my_image.filter(ImageFilter.SHARPEN)<br>
#save the image<br>
sharp.save('D:/image_sharpen.jpg')<br>
sharp.show()<br>
plt.imshow(sharp)<br>
plt.show()<br>
**Output:**<br>
![image](https://user-images.githubusercontent.com/97940058/179959511-b9a2a7f4-91cf-463d-b615-00cfb01509bc.png)<br>
![image](https://user-images.githubusercontent.com/97940058/179959603-37ee580e-e954-4757-a1d3-362c4ae76cdf.png)<br>

#Image flip<br>
import matplotlib.pyplot as plt<br>
#Load the image<br>
img= Image.open('lion.jpg')<br>
plt.imshow(img)<br>
plt.show()<br>
#use the flip function<br>
flip = img.transpose(Image.FLIP_LEFT_RIGHT)<br>
#save the image<br>
flip.save('D:/image_flip.jpg')<br>
plt.imshow(flip)<br>
plt.show()<br>
**Output:**<br>
![image](https://user-images.githubusercontent.com/97940058/179960397-0faff5a7-3f68-45cd-823e-82820c08d31d.png)<br>

#Importing Image class from PIL module<br>
from PIL import Image<br>
import matplotlib.pyplot as plt<br>
#opens a image in RGB mode<br>
im=Image.open('lion.jpg')<br>
#size of the image in pixels (size of original image)<br>
#(This is not mandatory)<br>
width, height = im.size<br>
#Cropped image of above dimension<br>
# (It will not change original image)<br>
im1=im.crop((280,100,800,600))<br>
#shows the image in image viewer<br>
im1.show()<br>
plt.imshow(im1)<br>
plt.show()<br>
**Output:**<br>
![image](https://user-images.githubusercontent.com/97940058/179961102-410908b3-5cf6-4b69-8e27-12502bfe132a.png)<br>


            




























  






























 






