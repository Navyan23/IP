# IP
# **1.Develop a program to display a grayscale image using read and write operations**<br>
import cv2<br>
img=cv2.imread('img.jpg',0)<br>
cv2.imshow('image',img)<br>
cv2.waitKey(0)<br>
cv2.destroyAllWindows()<br>

**Output:**<br>
![image](https://user-images.githubusercontent.com/97940058/173810505-979b82e1-7cc9-4eb1-a8ff-50228060d653.png)<br>
*************************************************************************************************************************<br>

# **2.Develop a program to display the image using mat plot lib**<br>
import matplotlib.image as mping<br>
import matplotlib.pyplot as plt<br>
img=mping.imread('img.jpg')<br>
plt.imshow(img)<br>

**Output:**<br>
![image](https://user-images.githubusercontent.com/97940058/173811930-e9e160ea-d325-4c99-a3dd-c41bdec26649.png)<br>


# **3.Develop a program to perform a linear transformation**<br>
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


# **4.Develop a program to conver color tree to Rgb Color values**<br>
from PIL import ImageColor<br>
img1=ImageColor.getrgb("yellow")<br>
print(img1)<br>
img2=ImageColor.getrgb("red")<br>
print(img2)<br>

**Output:**<br>
![image](https://user-images.githubusercontent.com/97940058/173814321-0f9c723c-4bb6-4796-838a-55a29b425b5f.png)<br>

# **5.Write a program to create image using a color**<br>
from PIL import Image<br>
img=Image.new('RGB',(200,400),(255,255,0))<br>
img.show()<br>

**Output:**<br>
![image](https://user-images.githubusercontent.com/97940058/173815086-5e10e1e1-ee52-4821-8b0a-11fec815e210.png)<br>

# **6.Develop a program to visualize the image using various color spaces**<br>
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


# **7.Write a program to display the image attributes**<br>
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


# **8.Develop a program to conver the original image to gray scale and then to binary**<br>
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

# **9.Resize the original image**<br>
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


# **10.Develop a program to read an image using URL**<br>
from skimage import io
import matplotlib.pyplot as plt<br>
url='https://images.unsplash.com/photo-1600703136783-bdb5ea365239?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8Mnx8cmVkJTIwZmxvd2VyfGVufDB8fDB8fA%3D%3D&w=1000&q=80'
image=io.imread(url)<br>
plt.imshow(image)<br>
plt.show()<br>

**Output:**<br>
![image](https://user-images.githubusercontent.com/97940058/175257948-78fe3194-63c7-46d2-8abe-56021d6bdd55.png)<br>


# **11.Develop a program to mask and blur the image**<br>
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


# **12.Develop a program to perform arithmatic operations on image**<br>
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



# **13.Develop a program to change the image to different color spaces**<br>
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


# **14.Develop a program to create an image using 2D array**<br>
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

# **15.program to perform bitwise operations**<br>
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


# **16.program to blurring image**<br>
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



# **17.program to perform image enhancement**<br>
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


# **18.program to perform morphological operations**<br>
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


# **19.Program to perform (i)  Read the image,convert it into grayscale image (ii) write(save) the grayscale image and (iii)dispaly the original image and grayscale image**<br>

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


# **20.Program to perform slicing with background**<br>
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



# **21.Program to perform slicing without background**<br>
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



# **22.Develop a program to analize the image data using histogram with opencv**<br>

import cv2<br>
from matplotlib import pyplot as plt<br>
img = cv2.imread('dog.jpg',0)<br>
plt.hist(img.ravel(),256,[0,256])<br>
plt.show()<br>
**Output:**<br>
![image](https://user-images.githubusercontent.com/97940058/178958471-7b9a75a4-921c-458a-91f9-eb40d4f6ce09.png)<br>
 
# **23.Develop a program to analize the image data using histogram with matplotlib**<br>
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

# **24.Develop a program to analize the image data using histogram with  skimage** <br>
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

# **25.Develop a program to analize the image data using histogram with  numpy(1)**<br>
import cv2<br>
import numpy as np<br>
img=cv2.imread('dog.jpg')<br>
hist=cv2.calcHist([img],[0],None,[256],[0,256])<br>
plt.hist(img.ravel(),256,[0,256])<br>
plt.show()<br>
**output:**<br>
![image](https://user-images.githubusercontent.com/97940058/178960477-2e3f5d15-af76-48ae-95b5-931be5e26adc.png)<br>


# **26.Develop a program to analize the image data using histogram with numpy(2)**<br>
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

# **27.program to perform basic image data analysis using intesity transformation: a)image negative b)log transformation c)gamma correction**<br>
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

# **28.program to perform basic imafe manipulations: a)Sharpness b)Flipping c)Cropping**<br>
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
#(It will not change original image)<br>
im1=im.crop((280,100,800,600))<br>
#shows the image in image viewer<br>
im1.show()<br>
plt.imshow(im1)<br>
plt.show()<br>
**Output:**<br>
![image](https://user-images.githubusercontent.com/97940058/179961102-410908b3-5cf6-4b69-8e27-12502bfe132a.png)<br>

# **29.Program to conver image to matrix**<br>
from PIL import Image<br>
from numpy import asarray<br>
img = Image.open('btf.jpg')<br>
numpydata = asarray(img)<br>
print(numpydata)<br>
**Output**<br>
[[[  8  10  22]<br>
  [  8  10  22]<br>
  [  8  10  22]<br>
  ...<br>
  [ 51  46 130]<br>
  [ 56  50 138]<br>
  [ 58  53 143]]<br><br>

 [[  8  10  22]<br>
  [  8  10  22]<br>
  [  8  10  22]<br>
  ...<br>
  [ 53  48 132]<br>
  [ 57  51 139]<br>
  [ 60  55 145]]<br>

 [[  8  10  22]<br>
  [  8  10  22]<br>
  [  8  10  22]<br>
  ...<br>
  [ 53  47 133]<br>
  [ 58  52 140]<br>
  [ 62  57 149]]<br>

 ...<br>

 [[  5   8  15]<br>
  [  5   8  15]<br>
  [  5   8  15]<br>
  ...<br>
  [ 11  13  28]<br>
  [ 11  13  28]<br>
  [ 11  13  28]]<br><br>

 [[  5   8  15]<br>
  [  5   8  15]<br>
  [  5   8  15]<br>
  ...<br>
  [ 11  13  28]<br>
  [ 11  13  28]<br>
  [ 11  13  28]]<br>

 [[  5   8  15]<br>
  [  5   8  15]<br>
  [  5   8  15]<br>
  ...<br>
  [ 11  13  28]<br>
  [ 11  13  28]<br>
  [ 11  13  28]]]<br>
  
  **30.Program (box)**<br>
  from PIL import Image<br>
import matplotlib.pyplot as plt<br>
  
#Create an image as input:<br>
input_image = Image.new(mode="RGB", size=(1000, 1000),color="pink")<br>
  
#save the image as "input.png"<br>
#(not mandatory)<br>
#input_image.save("input", format="png")<br>
  
#Extracting pixel map:<br>
pixel_map = input_image.load()<br>
  
#Extracting the width and height<br>
#of the image:<br>
width, height = input_image.size<br>
z = 100<br>
for i in range(width):<br>
    for j in range(height):<br>
        
        #the following if part will create<br>
        #a square with color orange<br>
        if((i >= z and i <= width-z) and (j >= z and j <= height-z)):<br>
            
            #RGB value of orange.<br>
            pixel_map[i, j] = (230,230,250)<br>
  
        #the following else part will fill the<br>
        #rest part with color light salmon.<br>
        else:<br>
            
            #RGB value of light salmon.<br>
            pixel_map[i, j] = (216,191,216)<br>
  
#The following loop will create a cross<br>
#of color blue.<br>
for i in range(width):<br>
    
    #RGB value of Blue.<br>
    pixel_map[i, i] = (0, 0, 255)<br>
    pixel_map[i, width-i-1] = (0, 0, 255)<br>
  
#Saving the final output<br>
#as "output.png":<br>
#input_image.save("output", format="png")
plt.imshow(input_image)
plt.show()  <br>
#use input_image.show() to see the image on the<br>
#output screen.<br>
  
            
**Output:**<br>
![image](https://user-images.githubusercontent.com/97940058/180191124-f49217ea-724a-486d-beaf-4f9e6ba6685c.png)<br>

**31.Write a program to  (circle)**<br>
import numpy as np<br>
import matplotlib.pyplot as plt<br>

arr = np.zeros((256,256,3), dtype=np.uint8)<br>
imgsize = arr.shape[:2]<br>
innerColor = (255, 255, 255)<br>
outerColor = (0, 0, 0)<br>
for y in range(imgsize[1]):<br>
    for x in range(imgsize[0]):<br>
        #Find the distance to the center<br>
        distanceToCenter = np.sqrt((x - imgsize[0]//2) ** 2 + (y - imgsize[1]//2) ** 2)<br>

        #Make it on a scale from 0 to 1innerColor<br>
        distanceToCenter = distanceToCenter / (np.sqrt(2) * imgsize[0]/2)<br>

        #Calculate r, g, and b values<br>
        r = outerColor[0] * distanceToCenter + innerColor[0] * (1 - distanceToCenter)<br>
        g = outerColor[1] * distanceToCenter + innerColor[1] * (1 - distanceToCenter)<br>
        b = outerColor[2] * distanceToCenter + innerColor[2] * (1 - distanceToCenter)<br>
        #print r, g, b<br>
        arr[y, x] = (int(r), int(g), int(b))<br>

plt.imshow(arr, cmap='gray')<br>
plt.show()<br>

**Output:**<br>
![image](https://user-images.githubusercontent.com/97940058/180191649-c5257e4d-fccc-4b25-9103-1ff10b18badc.png)<br>


# **32.Program to**<br>

import numpy as np<br>
import matplotlib.pyplot as plt<br>
imgsize=(650,650)<br>
image = Image.new('RGBA', imgsize)<br>
innerColor = [153,0,0]<br>
for y in range(imgsize[1]):<br>
    for x in range(imgsize[0]):<br>
         distanceToCenter =np.sqrt((x - imgsize[0]/2) ** 2 + (y - imgsize[1]/2) ** 2)<br>
         distanceToCenter = (distanceToCenter) / (np.sqrt(2) * imgsize[0]/2)<br>
         r = distanceToCenter + innerColor[0] * (1 - distanceToCenter)<br>
         g =  distanceToCenter + innerColor[1] * (1 - distanceToCenter)<br>
         b =  distanceToCenter + innerColor[2] * (1 - distanceToCenter)<br>
         image.putpixel((x, y), (int(r), int(g), int(b)))<br>
        
plt.imshow(image)<br>
plt.show()  <br>

**Output:**<br>
![image](https://user-images.githubusercontent.com/97940058/180192229-8c728d66-39c3-435a-af2b-f4be628970bb.png)<br>


**33.program**<br>
from PIL import Image<br>
import numpy as np<br>
import matplotlib.pyplot as plt<br>
w, h = 512, 512<br>
data = np.zeros((h, w, 3), dtype=np.uint8)<br>
data[0:120, 0:512] = [255, 255, 255]<br>
data[120:256, 0:512] = [218, 218, 218]<br>
data[256:320, 0:512] = [0, 0,0]<br>
data[320:420, 0:512] = [218, 218,218]<br>
data[420:512, 0:512] = [255, 255,255]<br>
#red patch in upper left<br>
img = Image.fromarray(data, 'RGB')<br>
img.save('img8.jpg')<br>
img.show()<br>
plt.imshow(img)<br>

**Output:**<br>
![image](https://user-images.githubusercontent.com/97940058/181223252-d6651dad-1ba4-41fe-ab05-bdfba75839f1.png)<br>


# **34.Program to find max pixel value from the image**<br>
import cv2<br>
import numpy as np<br>
import matplotlib.pyplot as plt<br>
img=cv2.imread('F3.jpg' )<br>
plt.imshow(img)<br>
plt.show()<br>
max_channels = np.amax([np.amax(img[:,:,0]), np.amax(img[:,:,1]),np.amax(img[:,:,2])])<br>
print(max_channels)<br>

**Output:**<br>
![image](https://user-images.githubusercontent.com/97940058/181223732-e8f2da86-b25b-4de0-866f-20bbe6969790.png)<br><br>


# **35.Program to find minimum pixel value from the image**<br>
import cv2<br>
import numpy as np<br>
import matplotlib.pyplot as plt<br>
img=cv2.imread('F3.jpg' )<br>
plt.imshow(img)<br>
plt.show()<br>
min_channels = np.amin([np.min(img[:,:,0]), np.amin(img[:,:,1]),np.amin(img[:,:,2])])<br>
print(min_channels)<br>
**Output:**
![image](https://user-images.githubusercontent.com/97940058/181224150-97f3c306-36ef-40d6-ad4b-1fb1b9b0eb46.png)<br>


# **36.program to find average pixel value from the image**<br>
import cv2<br>
import matplotlib.pyplot as plt<br>
img=cv2.imread("F3.JPG",0)<br>
img=cv2.cvtColor(img,cv2.COLOR_BGR2RGB)<br>
plt.imshow(img)<br>
np.average(img)<br>
**Output:**<br>
![image](https://user-images.githubusercontent.com/97940058/181224504-9f4ad5e5-9fd8-43e2-ae98-d36de7ccffdb.png)<br>


# **37.Program to find standard deviation**<br>
from PIL import Image,ImageStat<br>
import matplotlib.pyplot as plt<br>
im=Image.open('F3.jpg')<br>
plt.imshow(im)<br>
plt.show()<br>
stat=ImageStat.Stat(im)<br>
print(stat.stddev)<br>
**Output**<br>
![image](https://user-images.githubusercontent.com/97940058/181225066-bd3edfa0-e45b-4b3d-b329-94f32842fe81.png)<br>

# **38.Python3 program for printing the rectangular pattern**<br>
 
#Function to print the pattern<br>
def printPattern(n):<br>
 
    arraySize = n * 2 - 1;<br>
    result = [[0 for x in range(arraySize)]<br>
                 for y in range(arraySize)];<br>
         
    #Fill the values<br>
    for i in range(arraySize):<br>
        for j in range(arraySize):<br>
            if(abs(i - (arraySize // 2)) ><br>
               abs(j - (arraySize // 2))):<br>
                result[i][j] = abs(i - (arraySize // 2)) ;<br>
            else:<br>
                result[i][j] = abs(j - (arraySize // 2)) ;<br>
             
    #Print the array<br>
    for i in range(arraySize):<br>
        for j in range(arraySize):<br>
            print(result[i][j], end = " ");<br>
        print("");<br>
 
#Driver Code<br>
n = 3;<br>
 
printPattern(n);<br>
**Output:**<br>
![image](https://user-images.githubusercontent.com/97940058/181439288-23c6652b-74ab-4371-ace2-fb420765e770.png)<br>


# **39.Edge detection**<br>
import cv2<br>
#Read the original image<br>
img = cv2.imread('lion.jpg')<br>
#Display original image<br>
cv2.imshow('Original', img)<br>
cv2.waitKey(0)<br>
#Convert to graycsale<br>
img_gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)<br>
#Blur the image for better edge detection<br>
img_blur = cv2.GaussianBlur(img_gray, (3,3), 0)<br>
<br>
#Sobel Edge Detection<br>
sobelx = cv2.Sobel(src=img_blur, ddepth=cv2.CV_64F, dx=1, dy=0, ksize=5) #Sobel Edge Detection on the X axis<br>
sobely = cv2.Sobel(src=img_blur, ddepth=cv2.CV_64F, dx=0, dy=1, ksize=5) #Sobel Edge Detection on the Y axis<br>
sobelxy = cv2.Sobel(src=img_blur, ddepth=cv2.CV_64F, dx=1, dy=1, ksize=5) #Combined X and Y Sobel Edge Detection<br>
#Display Sobel Edge Detection Images<br>
cv2.imshow('Sobel X', sobelx)<br>
cv2.waitKey(0)<br>
cv2.imshow('Sobel Y', sobely)<br>
cv2.waitKey(0)<br>
cv2.imshow('Sobel X Y using Sobel() function', sobelxy)<br>
cv2.waitKey(0)<br>
#Canny Edge Detection<br>
edges = cv2.Canny(image=img_blur, threshold1=100, threshold2=200) # Canny Edge Detection<br>
#Display Canny Edge Detection Image<br>
cv2.imshow('Canny Edge Detection', edges)<br>
cv2.waitKey(0)<br>
cv2.destroyAllWindows()<br>
**Result**<br>
![image](https://user-images.githubusercontent.com/97940058/186392552-999a7b27-8091-41eb-8117-6679d55049a5.png)<br>
![image](https://user-images.githubusercontent.com/97940058/186393554-d78cbd77-b17d-43eb-901f-efeefd8d0f86.png)<br>
![image](https://user-images.githubusercontent.com/97940058/186393709-7725906a-582d-4467-9d34-74a5306578f3.png)<br>
![image](https://user-images.githubusercontent.com/97940058/186394092-68388921-f626-497b-b3d9-a0c5a9572375.png)<br>
![image](https://user-images.githubusercontent.com/97940058/186394292-bbd147f2-e487-4e6c-ae20-f42d7e972a40.png)<br>

# **40.Basic pillow operations**<br>
from PIL import Image,ImageChops,ImageFilter<br>
from matplotlib import pyplot as plt<br>
#create a PIL Image objects<br>
x = Image.open("x.png")<br>
o = Image.open("o.png")<br>
#Find out attributes of Image objects<br>
print('size of the image: ',x.size, 'colour mode:',x.mode)<br>
print('size of the image: ',o.size, 'colour mode:',o.mode)<br>
#plot 2 images one besides the other<br>
plt.subplot(121), plt.imshow(x)<br>
plt.axis('off')<br>
plt.subplot(122), plt.imshow(o)<br>
plt.axis('off')<br>
#multiply images<br>
merged = ImageChops.multiply(x,o)<br>
#adding 2 images<br>
add = ImageChops.add(x,o)<br>
#convert colour mode<br>
greyscale = merged.convert('L')<br>
greyscale<br>
**Output:**<br>
![image](https://user-images.githubusercontent.com/97940058/187873096-1d277034-efcd-435d-9038-ed0d8650aa15.png)<br>

# **More attributes**<br>
image = merged<br>
print('image size:',image.size,<br>
     '\ncolor mode:',image.mode,<br>
     '\nimage width :',image.width,'|also represented by:',image.size[0],<br>
     '\nimage height:',image.height,'|also represented by:',image.size[1],)<br>
**Output:**<br>
image size: (256, 256) <br>
color mode: RGB <br>
image width : 256 |also represented by: 256 <br>
image height: 256 |also represented by: 256<br>

# **mapping the pixels of the image so we can use them as coordinates**<br>
pixel = greyscale.load()<br>
#a nested loop to parse through all the pixels in the image<br>
for row in range(greyscale.size[0]):<br>
    for column in range(greyscale.size[1]):<br>
        if pixel[row,column]!=(255):<br>
            pixel[row,column]=(0)<br>
greyscale<br>
**Output:**
![image](https://user-images.githubusercontent.com/97940058/187873955-bc36f4f8-2585-4533-a989-54920bcac884.png)<br>

# **1.invert image**<br>
invert = ImageChops.invert(greyscale)<br>
#2.invert by subtraction<br>
bg = Image.new('L',(256,256),color=(255))#create a new image with a solid white background<br>
subt=ImageChops.subtract(bg,greyscale)#subtract image from background<br>
#3.rotate<br>
rotate = subt.rotate(45)<br>
rotate<br>
**Output:<br>
![image](https://user-images.githubusercontent.com/97940058/187874423-25a51aa3-f411-4a49-8f01-df6fd8cee814.png)<br>

# **gaussian blur**<br>
blur=greyscale.filter(ImageFilter.GaussianBlur(radius=1))<br>
#edge detection<br>
edge=blur.filter(ImageFilter.FIND_EDGES)<br>
edge<br>
**Output:**<br>
![image](https://user-images.githubusercontent.com/97940058/187874904-d3e45501-5156-43ce-bcf4-ac776e4529cf.png)<br>

# **change edge colours**<br>
edge=edge.convert('RGB')<br>
bg_red=Image.new('RGB',(256,256),color=(255,0,0))<br>
filled_edge=ImageChops.darker(bg_red,edge)<br>
filled_edge<br>
**Output:**<br>
![image](https://user-images.githubusercontent.com/97940058/187875170-458aade7-0b0e-4223-8df7-69f26761b231.png)<br>

# **save in the directory**<br>
edge.save('processed.png')<br>

# **41.(1) Image restoration:**<br>
**a) Restore a damaged image**<br>
import numpy as np<br>
import cv2<br>
import matplotlib.pyplot as plt<br>
#Open the image.<br>
img =cv2.imread('dimage_damaged.png')<br>
plt.imshow(img)<br>
plt.show()<br>
#Load the mask.<br>
mask= cv2.imread('dimage_mask.png', 0)<br>
plt.imshow(mask)<br>
plt.show()<br>
#Inpaint.<br>
dst = cv2.inpaint (img, mask, 3, cv2.INPAINT_TELEA)<br>
#write the output.<br>
cv2.imwrite('dimage_inpainted.png', dst)<br>
plt.imshow(dst)<br>
plt.show()<br>**Output:**<br>
![image](https://user-images.githubusercontent.com/97940058/187877524-7a008fd9-4071-45e3-9762-019f0e0447d8.png)<br>
![image](https://user-images.githubusercontent.com/97940058/187877675-0f9f8d72-06d0-4cfd-a8fd-e9819fa02df4.png)<br>

 **(b) Removing Logo’s:**<br>
import numpy as np<br>
import matplotlib.pyplot as plt<br>
import pandas as pd<br>
plt.rcParams['figure.figsize'] = (10, 8)<br>

def show_image (image, title='Image', cmap_type='gray'): <br>
        plt.imshow(image, cmap=cmap_type)<br>
        plt.title(title)<br>
        plt.axis('off')<br>
def plot_comparison(img_original, img_filtered, img_title_filtered):<br>
    fig, (ax1, ax2)= plt.subplots (ncols=2, figsize=(10, 8), sharex=True, sharey=True) <br>
    ax1.imshow(img_original, cmap=plt.cm.gray)<br>
    ax1.set_title('Original')<br>
    ax1.axis('off')<br>
    ax2.imshow(img_filtered, cmap=plt.cm.gray)<br>
    ax2.set_title(img_title_filtered)<br>
    ax2.axis('off')<br>
    
from skimage.restoration import inpaint<br><br>
from skimage.transform import resize<br>
from skimage import color<br>

mage_with_logo = plt.imread('imlogo.png')<br>
#Initalize the mask<br>
mask = np.zeros(image_with_logo.shape[:-1])<br>
#Set the pixels where the logo is to 1<br>
mask[210:272,360:425] = 1<br>
#Apply inpainting to remove the logo<br>
image_logo_removed = inpaint.inpaint_biharmonic(image_with_logo,<br>
                                              mask,<br>
                                              multichannel=True)<br>
#Show the original and logo removed images<br>
plot_comparison(image_with_logo,image_logo_removed,'Image with logo removed')<br>
**Output:**<br>
![image](https://user-images.githubusercontent.com/97940058/187878452-00af3ead-a01c-4152-abd6-512c67cb27c9.png)<br>

# **(2) Noise:** <br>
**(a) Adding noise**<br>
from skimage.util import random_noise<br>
fruit_image = plt.imread('fruitts.jpg')<br>
#Add noise to the image<br>
noisy_image = random_noise (fruit_image)<br>
#Show th original and resulting image<br>
plot_comparison (fruit_image, noisy_image, 'Noisy image')<br>
**Output:**<br>
![image](https://user-images.githubusercontent.com/97940058/187878985-c95c3bbe-12e3-473a-872a-f8c97019775d.png)<br>

**(b) Reducing Noise**<br>
from skimage.restoration import denoise_tv_chambolle<br>
noisy_image = plt.imread('noisy.jpg')<br>
#Apply total variation filter denoising<br>
denoised_image = denoise_tv_chambolle (noisy_image, multichannel=True)<br>
#Show the noisy and denoised image<br>
plot_comparison (noisy_image, denoised_image, 'Denoised Image')<br>
**Output:**<br>
![image](https://user-images.githubusercontent.com/97940058/187879603-11789e91-2e85-429e-88fd-7dafce85792c.png)<br>

**(c) Reducing Noise while preserving edges**<br>
from skimage.restoration import denoise_bilateral<br>
landscape_image = plt.imread('noisy.jpg')<br>
#Apply bilateral filter denoising<br>
denoised_image = denoise_bilateral (landscape_image, multichannel=True)<br>
#Show original and resulting images<br>
plot_comparison (landscape_image, denoised_image, 'Denoised Image')<br>
**Output**<br>
![image](https://user-images.githubusercontent.com/97940058/187879998-032ec565-57cd-4436-aed7-fa1bf38a3de6.png)<br>

# **(3) Segmentation :**<br>
**(a) Superpixel Segmentation**<br>
from skimage.segmentation import slic<br>
from skimage.color import label2rgb<br>
face_image = plt.imread('face.jpg')<br>
#Obtain the segmentation with 400 regions <br>
segments = slic (face_image, n_segments=400)<br>
#Put segments on top of original image to compare<br>
segmented_image = label2rgb(segments, face_image, kind='avg')<br>
#Show the segmented image<br>
plot_comparison (face_image, segmented_image, 'Segmented image, 400 superpixels')<br>
**Output**<br>
![image](https://user-images.githubusercontent.com/97940058/187881525-f61a43cc-b2b0-415a-bfd7-8e0b6e5a5b3f.png)<br>

# **(4) Contours:**<br>
**(a) Contouring shapes**<br>
def show_image_contour (image, contours):<br>
    plt.figure()<br>
    for n, contour in enumerate(contours):<br>
        plt.plot(contour[:, 1], contour[:, 0], linewidth=3) <br>
    plt.imshow(image, interpolation='nearest', cmap='gray_r')<br>
    plt.title('Contours')<br>
    plt.axis('off')<br>
    
from skimage import measure, data<br>
#Obtain the horse image<br>
horse_image = data.horse()<br>
#Find the contours with a constant Level value of 0.8 <br>
contours = measure.find_contours (horse_image, level=0.8)<br>
#Shows the image with contours found <br>
show_image_contour (horse_image, contours)<br>
**Output**<br>
![image](https://user-images.githubusercontent.com/97940058/187882088-9f0e74fa-b3b9-4971-941d-b14a07bd27bc.png)<br>

**(b) Find contours of an image that is not binary**<br>
from skimage.io import imread<br>
from skimage.filters import threshold_otsu<br>

image_dices = imread('diceimg.png')<br>

#Make the image grayscale <br>
image_dices =color.rgb2gray(image_dices)<br>

#obtain the optimal thresh value<br>
thresh = threshold_otsu(image_dices)<br>

#Apply thresholding<br>
binary = image_dices > thresh<br>

#Find contours at a constant value of 0.8<br>
contours = measure.find_contours(binary, level=0.8)<br>

#Show the image<br>
show_image_contour(image_dices, contours)<br>
**Output**<br>
![image](https://user-images.githubusercontent.com/97940058/187882472-1187cfa5-3a72-473e-b28a-cb6c47f65ba6.png)<br>

**(c) Count the dots in a dice's image**<br>
shape_contours = [cnt.shape[0] for cnt in contours]<br>

#Set 50 as the maximum size of the dots shape<br>
max_dots_shape = 50<br>

#Count dots in contours excluding bigger than dots size <br>
dots_contours = [cnt for cnt in contours if np.shape (cnt) [0] < max_dots_shape]<br>

#Shows all contours found <br>
show_image_contour (binary, contours)<br>

#Print the dice's number<br>
print('Dices dots number: {}.'.format(len(dots_contours)))<br>
**Output:**<br>
![image](https://user-images.githubusercontent.com/97940058/187883109-ca913890-32f5-4088-8fbe-b52655f38da4.png)<br>

# **Implement a program to perform various edge detection techniques**<br>
**a) Canny Edge detection**<br>
#Canny Edge detection<br>
import cv2<br>
import numpy as np<br>
import matplotlib.pyplot as plt<br>
plt.style.use('seaborn')<br>
loaded_image = cv2.imread("imgsh.png")<br>
loaded_image = cv2.cvtColor(loaded_image,cv2.COLOR_BGR2RGB)<br>
gray_image = cv2.cvtColor(loaded_image,cv2.COLOR_BGR2GRAY)<br>
edged_image = cv2.Canny(gray_image, threshold1=30, threshold2=100)<br>
plt.figure(figsize=(20,20))<br>
plt.subplot(1,3,1)<br>
plt.imshow(loaded_image, cmap="gray")<br>
plt.title("original Image")<br>
plt.axis("off")<br>
plt.subplot(1,3,2)<br>
plt.imshow(gray_image,cmap="gray")<br>
plt.axis("off")<br>
plt.title("GrayScale Image")<br>
plt.subplot(1,3,3)<br>
plt.imshow(edged_image,cmap="gray")<br>
plt.axis("off")<br>
plt.title("Canny Edge Detected Image")<br>
plt.show()**Output**<br>
![image](https://user-images.githubusercontent.com/97940058/187900557-35f54413-d448-4b40-8d97-f3e3ebbc42b4.png)<br>

**b) Edge detection schemes - the gradient (Sobel - first order derivatives)<br>
based edge detector and the Laplacian (2nd order derivative, so it is<br>
extremely sensitive to noise) based edge detector.**<br>
#Laplacian and Sobel Edge detecting methods<br>
import cv2
import numpy as np<br>
from matplotlib import pyplot as plt<br>
#Loading image<br><br>
#imge = cv2.imread('SanFrancisco.jpg',) <br>
imge = cv2.imread('imgsh.png',)<br>
#converting to gray scale<br>
gray = cv2.cvtColor(imge, cv2.COLOR_BGR2GRAY)<br>
#remove noise<br>
img = cv2.GaussianBlur (gray,(3,3),0)<br>
#convolute with proper kernels<br>
laplacian = cv2.Laplacian (img,cv2.CV_64F)<br>
sobelx = cv2.Sobel(img,cv2.CV_64F,1,0,ksize=5) # x <br>
sobely = cv2.Sobel(img,cv2.CV_64F,0,1,ksize=5) # y<br>
plt.subplot(2,2,1), plt.imshow(img,cmap = 'gray')<br>
plt.title('Original'), plt.xticks([]), plt.yticks([])<br>
plt.subplot(2,2,2), plt.imshow(laplacian, cmap = 'gray')<br>
plt.title('Laplacian'), plt.xticks([]), plt.yticks([])<br>
plt.subplot(2,2,3), plt.imshow(sobelx, cmap = 'gray')<br>
plt.title('Sobel x'), plt.xticks([]), plt.yticks([])<br> 
plt.subplot(2,2,4), plt.imshow(sobely,cmap = 'gray')<br>
plt.title('Sobel Y'), plt.xticks([]), plt.yticks([])<br>
plt.show()<br>
**Output:**<br>
![image](https://user-images.githubusercontent.com/97940058/187901054-ea9e8109-c552-471d-b427-8b7b2b2c415e.png)<br>

**c) Edge detection using Prewitt Operator**<br>
import cv2<br>
import numpy as np<br>
from matplotlib import pyplot as plt <br>
img = cv2.imread('imgsh.png')<br>
gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)<br>
img_gaussian = cv2.GaussianBlur (gray, (3,3),0)<br>
#prewitt<br>
kernelx = np.array([[1,1,1], [0,0,0],[-1,-1,-1]])<br><br>
kernely = np.array([[-1,0,1],[-1,0,1],[-1,0,1]])<br>
img_prewittx = cv2.filter2D (img_gaussian, -1, kernelx) <br>
img_prewitty = cv2.filter2D(img_gaussian, -1, kernely)<br>
cv2.imshow("Original Image", img)<br>
cv2.imshow("Prewitt x", img_prewittx)<br>
cv2.imshow("Prewitt y", img_prewitty)<br>
cv2.imshow("Prewitt", img_prewittx + img_prewitty)<br>
cv2.waitKey()<br>
cv2.destroyAllwindows()<br>
**Output:**<br>
![image](https://user-images.githubusercontent.com/97940058/187902022-65b43a7a-a0ba-4b3c-90bf-6107a1c4ac32.png)<br>
![image](https://user-images.githubusercontent.com/97940058/187902113-7f67d1df-a5cf-486f-94bd-679953a5e14e.png)<br>
![image](https://user-images.githubusercontent.com/97940058/187902193-4e066b08-ba19-45be-831b-3f7df2d1c11b.png)<br>
![image](https://user-images.githubusercontent.com/97940058/187902262-84529015-0244-44ac-9457-22123d229f18.png)<br>
<br>
**d) Roberts Edge Detection- Roberts cross operator**<br>
#Roberts Edge Detection- Roberts cross operator<br>
import cv2<br>
import numpy as np<br>
from scipy import ndimage<br>
from matplotlib import pyplot as plt<br>
roberts_cross_v = np.array([[1, 0],<br>
                            [0,-1]])<br>
roberts_cross_h = np.array([[0, 1],<br>        
                            [-1, 0 ]] )<br>
img = cv2.imread("imgsh.png",0).astype('float64')<br>
img/=255.0<br>
vertical = ndimage.convolve( img, roberts_cross_v )<br>
horizontal=ndimage.convolve( img, roberts_cross_h)<br>
edged_img = np.sqrt( np.square (horizontal) + np.square (vertical))<br>
edged_img*=255<br>
cv2.imwrite("output.jpg",edged_img)<br>
cv2.imshow("OutputImage", edged_img)<br>
cv2.waitKey()<br>
cv2.destroyAllWindows()<br>
**Output:**<br>
![image](https://user-images.githubusercontent.com/97940058/187902786-34b62fc8-acc2-4c54-b662-df6f03ff62d5.png)<br>



















































    
    
 










            




























  






























 






