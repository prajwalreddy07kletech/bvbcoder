# bvbcoder
this is my first repositary. 
<br>
owner = prajwal biradar
<br>
my friend is athrav adake and sagar.

import numpy as np
import matplotlib.pyplot as plt
from PIL import Image

img_pil = Image.open(r"C:\Users\prajw\OneDrive\Pictures\pexels-bogdan-dirica-532600-1645668.jpg")
img_pil = img_pil.convert("RGB")
img = np.array(img_pil)
print("image shape (rows, cols, channels):", img.shape)

plt.figure(figsize=(4,4))
plt.imshow(img)
plt.title("exploration")
plt.axis("on")
plt.show()

i= 50
j = 80
pixel1 = img[i,j].reshape(3,1)
print("selected pixel location;",(i,j))
print("pixel1 RGB vector:\n",pixel1)

R = pixel1[0]
G = pixel1[1]
B = pixel1[2]

print("colour components: ")
print("..................")
print("Red : ",R)
print("Green : ",G)
print("Blue : ",B)

import warnings
warnings.filterwarnings("ignore")

import numpy as np
import matplotlib.pyplot as plt
from PIL import Image
pixel2 = img[i+1,j].reshape(3,1)
print("Nebhour pixcel location:",(i+1,j))
print("pixel2 RGB vector:\n",pixel2)

difference = pixel2 - pixel1
print("\nDifference vector:\n",difference)

dR = int(difference[0])
dG = int(difference[1])
dB = int(difference[2])
magnitude = (dR*dR*dG+dB*dB)
