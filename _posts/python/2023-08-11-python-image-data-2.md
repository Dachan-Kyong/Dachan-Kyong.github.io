---
title: "Image Data(2): PIL: Python Imaging Library"
author: Dachan Kyong
date: 2023-08-11 14:00:00 +0900
categories: [Python, Image Data]
tags: [python]
render_with_liquid: false
---

## About PIL: Python Imaging Library
`PIL` (Python imaging library) provides powerful tools for opening, manipulating, and performing various image processing tasks on image files. PIL allows you to load and save images, perform operations such as resizing, rotating, cropping, and more. It also offers features for applying filters, blurring effects, image composition, and other image effects. PIL is widely used in areas such as image processing, graphic design, computer vision, data visualization, and more.

PIL helps Python developers work with image-related tasks more easily, providing essential functionality for handling image data. It offers a simple and intuitive interface, making image processing accessible and user-friendly.



## Usages of PIL

### PIL Iinstallation
We can download `PIL` through macOS Terminal:
```bash
brew pip3 install pillow
```

We can use `PIL` for basic image data processing.

### PIL: Width & Height
I created image_analysis.py in the folder where I want to conduct my testing. And I created an assets > img folder to place the `yellow.png`, 360 X 360 yellow box image, to test:

This is the basic code to load and open an image, and then print it:


```bash
from PIL import Image

# Load the image
image_path = 'assets/img/yellow.png'
image = Image.open(image_path)

# Extract image dimensions
width, height = image.size

#Output
print("Image Size:", width, "X", height)
```
{: file='image_analysis.py'}

You can run the code using the following command:
```bash
python3 image_analysis.py // "this will run your **.py."
```
Expected Output:
```bash
Image Size: 360 X 360
```


## References
- <https://pillow.readthedocs.io/en/stable/>