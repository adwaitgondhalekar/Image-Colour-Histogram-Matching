# Image-Colour-Histogram-Matching

## Colour Histogram Matching is an Image Processing technique involving two Images.

### 1. Each Image has its own and unique Colour Histogram depending on the colours, brightness, contrast of the Image.
### 2. This code provides an easy way where an input image can be transformed according to the Colour Histogram of the reference Image.
### 3. Initially the input Image's Histogram is equalized by employing certain different mathematical methods such as CDF, PDF and corresponding equalized pixel level is calculated for each previous pixel level and their value is changed accordingly.
### 4.Next the Reference Image's Colour Histogram is equalized.
### 5. Finally a mapping is found out between the equalized pixels of the Input Image and the equalized pixels of the Reference Image.
### 6. The pixel values of the Input Image are changed accordingly where the aim of Matching Colour Histogram of Style Image with Reference Image is achieved.



## Detailed Steps -

### 1.Each Image has RGB Channels and in each of these channels there are pixels with varying intensity from 0-255 (total 256) i.e. Grayscale level
### 2.Next step is to calculate the probability disribution for each pixel in each of the RGB Channels. pdf = grayscale level / (image height * image weight)
### 3.Next up is to calculate cdf (cumulative distributive function) by adding up the probability distributions of the pixels.
### 4.Further the grayscale level of each pixel is to be equalized by calculating the product of the calculated cdf of each pixel and maximum grayscale level i.e. 255. Equalized_pixel_level = (cdf_of_pixel * max_grayscale_level)
### 5.The above steps are followed to equalize the content and style image.
### 6.Last step is to map the equalized pixels of the style image to the content image to get the Histogram Matched Style Image.
