# DIP
# 1. develop the program to perform linear configration on a image 
To rotate an image using OpenCV Python, first calculate the affine matrix that does the affine transformation 


import cv2
 
img = cv2.imread('images.jpg')

(r, c) = img.shape[:2]
                    
center = (w / 2, h / 2)
 
angle90 = 90
 
scale = 1.0
M = cv2.getRotationMatrix2D(center, angle90, scale)
rotated90 = cv2.warpAffine(img, M, (r, c))
cv2.imshow('Original Images',img)
cv2.waitKey(0) 
cv2.destroyAllWindows() 
 
cv2.imshow('Image rotated by 90 degrees',rotated90)
cv2.waitKey(0) 
cv2.destroyAllWindows() 


# original image

 ![image](https://user-images.githubusercontent.com/97161717/148200751-2446e808-d08b-4ba8-860c-0db317087fc6.png)

# rotated image
![image](https://user-images.githubusercontent.com/97161717/148200618-91048e78-4320-4cca-b4ac-5f6f94027937.png)
