# Homomorphic Filtering of colour images using a Spatial Filter Kernel in the HSI colour space

The algorithm used in this project is based on homomorphic filtering of color images, performed in the spatial domain, using the HSI color space. The method aims to improve image contrast and enhance details while maintaining low computational complexity and accurate color reproduction.

Homomorphic filtering is an image processing technique used to separate and treat illumination and reflectance differently. The basic model considers the image as a product between illumination and reflectance. By applying the logarithm, this product becomes a sum, which allows transformation into the frequency domain and the application of a filter that attenuates low frequencies and enhances high frequencies. Finally, the image is transformed back into the spatial domain through exponentiation.

The algorithm proposed in this project implements a direct approach in the spatial domain, using a small filtering kernel (3×3). This approach eliminates the need for more complex transformations, such as Fourier transforms, and also reduces computational complexity.

The use of a 3×3 filter provides a balance between contrast enhancement and preservation of high-frequency image details, without introducing visible artifacts or excessive edge blurring.

For color image processing, the algorithm uses the HSI (Hue, Saturation, Intensity) color space. Converting from the RGB color space to HSI allows the separation of intensity information from chromatic information. Therefore, the filtering is applied exclusively to the intensity channel (I), while the hue (H) and saturation (S) components remain unchanged. This prevents color distortions that may occur if filtering is performed directly on the RGB channels.
