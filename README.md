# Homomorphic Filtering of colour images using a Spatial Filter Kernel in the HSI colour space

The algorithm used in this project is based on homomorphic filtering of color images, performed in the spatial domain, using the HSI color space. The method aims to improve image contrast and enhance details while maintaining low computational complexity and accurate color reproduction.

Homomorphic filtering is an image processing technique used to separate and treat illumination and reflectance differently. The basic model considers the image as a product between illumination and reflectance. By applying the logarithm, this product becomes a sum, which allows transformation into the frequency domain and the application of a filter that attenuates low frequencies and enhances high frequencies. Finally, the image is transformed back into the spatial domain through exponentiation.

The algorithm proposed in this project implements a direct approach in the spatial domain, using a small filtering kernel (3×3). This approach eliminates the need for more complex transformations, such as Fourier transforms, and also reduces computational complexity.

The use of a 3×3 filter provides a balance between contrast enhancement and preservation of high-frequency image details, without introducing visible artifacts or excessive edge blurring.

For color image processing, the algorithm uses the HSI (Hue, Saturation, Intensity) color space. Converting from the RGB color space to HSI allows the separation of intensity information from chromatic information. Therefore, the filtering is applied exclusively to the intensity channel (I), while the hue (H) and saturation (S) components remain unchanged. This prevents color distortions that may occur if filtering is performed directly on the RGB channels.

# Setup for homomorphic spatial filtering of colour images in HSI colour space


<img width="648" height="91" alt="image" src="https://github.com/user-attachments/assets/b2d6be2f-94c2-4fcb-a956-c02208522aca" />


# Results

To observe how the homomorphic filter works, it was compared with a median filter and an arithmetic mean filter.
<img width="640" height="624" alt="image" src="https://github.com/user-attachments/assets/07445c5b-9a90-4bb9-935c-648736440b01" />

The two filters tested in these images have the function of reducing noise.

<img width="707" height="335" alt="image" src="https://github.com/user-attachments/assets/31c22bd9-b5dd-4b61-88b0-3bd86fab0eb6" />

<img width="665" height="280" alt="image" src="https://github.com/user-attachments/assets/a6cd5a2a-5184-4c93-9ea1-a05497675928" />

In conclusion, the arithmetic mean, median, and homomorphic filters using an arithmetic mean kernel have the ability to reduce image noise, while the adjusted high-pass kernel improves image quality by removing shadows and enhancing the overall contrast of the image.

