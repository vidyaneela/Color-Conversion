# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Import cv2 and save and image as filename.jpg

### Step2:
Use imread(filename, flags) to read the file.

### Step3:
Use cv2.cvtColor(src, code, dst, dstCn) to convert an image from one color space to another.

### Step4:
Split and merge the image using cv2.split and cv2.merge commands.

### Step5:
End the program and close the output image windows.

## Program:
```
# Developed By:VIDYA NEELA M
# Register Number:212221230120
```
### Original:
```
rick_color_image = cv2.imread('1bird.jpg')
cv2.imshow('image',rick_color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
# i) Convert BGR and RGB to HSV and GRAY

```
#BGR_2_HSV
hsvimg=cv2.cvtColor(rick_color_image,cv2.COLOR_BGR2HSV)
cv2.imshow('BGRhsv',hsvimg)

#RGB_2_HSV
hsvimg1=cv2.cvtColor(rick_color_image,cv2.COLOR_RGB2HSV)
cv2.imshow('RGBhsv',hsvimg1)

#RGB2GRAY
gray=cv2.cvtColor(rick_color_image,cv2.COLOR_RGB2GRAY)
cv2.imshow('grayRGB',gray)

#BGR2GRAY
gray1=cv2.cvtColor(rick_color_image,cv2.COLOR_BGR2GRAY)
cv2.imshow('grayBGR',gray1)
cv2.waitKey(0)
cv2.destroyAllWindows()

```


# ii)Convert HSV to RGB and BGR
```
#RGB to YCrCb
YCrCb_img=cv2.cvtColor(img,cv2.COLOR_RGB2YCrCb)
cv2.imshow('RGB2YCrCb',YCrCb_img)
cv2.waitKey(0)
cv2.destroyAllWindows()

#BGR TO YCrCb
YCrCb_img1=cv2.cvtColor(img,cv2.COLOR_BGR2YCrCb)
cv2.imshow('BGR2YCrCb',YCrCb_img1)
cv2.waitKey(0)
cv2.destroyAllWindows()

```


# iii)Convert RGB and BGR to YCrCb

```
blue=img[:,:,0]
green=img[:,:,1]
red=img[:,:,2]
cv2.imshow('B-Channel',blue)
cv2.imshow('G-Channel',green)
cv2.imshow('R-Channel',red)
merged_BGR=cv2.merge((blue,green,red))
cv2.imshow('Merged BGR Image',merged_BGR)
cv2.waitKey(0)
cv2.destoryAllWindows()

```


# iv)Split and Merge RGB Image
```
blue=img[:,:,0]
green=img[:,:,1]
red=img[:,:,2]
cv2.imshow('B-Channel',blue)
cv2.imshow('G-Channel',green)
cv2.imshow('R-Channel',red)
merged_BGR=cv2.merge((blue,green,red))
cv2.imshow('Merged BGR Image',merged_BGR)
cv2.waitKey(0)
cv2.destoryAllWindows()

```



# v) Split and merge HSV Image
```

#Split & merge hsv
hsv = cv2.cvtColor(img, cv2.COLOR_BGR2HSV)
h,s,v=cv2.split(hsv)
cv2.imshow("Hue-image",h)
cv2.imshow("Saturation-image",s)
cv2.imshow("Gray-image",v)
Merged_HSV=cv2.merge((h,s,v))
cv2.imshow('Merged HSV Image',Merged_HSV)
cv2.waitKey(0)
cv2.destoryAllWindows()


```

## Output:
### Original:

![image](https://user-images.githubusercontent.com/94169318/228281002-db659c9c-058b-4035-a0f1-396cdf970281.png)

### i) BGR and RGB to HSV and GRAY

![image](https://user-images.githubusercontent.com/94169318/228280045-25973d90-fbb0-42e2-9635-5d89d86648cd.png)


### ii) HSV to RGB and BGR
![image](https://user-images.githubusercontent.com/94169318/228277408-dbd5e20c-d8ec-46ea-b5f8-c19f7132a80c.png)


### iii) RGB and BGR to YCrCb

![image](https://user-images.githubusercontent.com/94169318/228281861-127fe0f4-2758-4826-8098-fba3727b9ec5.png)


### iv) Split and merge RGB Image

![image](https://user-images.githubusercontent.com/94169318/228282378-4acb6ba5-aa25-4aad-9a0b-09591c85673a.png)


### v) Split and merge HSV Image

![image](https://user-images.githubusercontent.com/94169318/228283888-4b7a117e-58dc-4870-a84a-992e73f098c3.png)


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
