# OpenCV Image Filter Studio

An interactive image filtering tool built with OpenCV and ipywidgets — apply artistic, edge, and colour filters to any image directly in Google Colab.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Ragul2526/opencv-image-filter-studio/blob/main/image_filter.ipynb)

---

## Filters available

| Category | Filters |
|----------|---------|
| Basic | Grayscale, Blur, Sharpen |
| Edge based | Canny Edge, Sobel Edge |
| Artistic | Cartoonify, Pencil Sketch, Emboss, Sepia |
| Colour | Warm Tone, Cool Tone, Invert |
| Portrait | Background Blur |

---

## How to use

1. Click the **Open in Colab** badge above
2. Run all cells
3. Click **Upload Image** to upload any image
4. Select a filter from the dropdown
5. Click **Apply Filter** to see the result
6. Click **Download Result** to save the filtered image

> No API keys or installations needed — runs entirely in Google Colab

---

## Results

### Grayscale
![Grayscale](Assets/gray_scale.png)

### Blur
![Blur](Assets/blur.png)

### Sharpen
![Sharpen](Assets/sharpen.png)

### Canny Edge
![Canny Edge](Assets/canny.png)

### Sobel Edge
![Sobel Edge](Assets/sobel.png)

### Cartoonify
![Cartoonify](Assets/cartoon.png)

### Pencil Sketch
![Pencil Sketch](Assets/sketch.png)

### Emboss
![Emboss](Assets/emboss.png)

### Sepia
![Sepia](Assets/sepia.png)

### Warm Tone
![Warm Tone](Assets/warm_tone.png)

### Cool Tone
![Cool Tone](Assets/cool_tone.png)

### Invert
![Invert](Assets/invert.png)

### Background Blur
![Background Blur](Assets/background_blur.png)

---

## How each filter works

| Filter | How it works |
|--------|-------------|
| Grayscale | Converts RGB to single channel using weighted average (0.299R + 0.587G + 0.114B) |
| Blur | Replaces each pixel with weighted average of neighbors using Gaussian kernel |
| Sharpen | Amplifies center pixel and subtracts neighbors using convolution kernel |
| Canny Edge | Detects edges using gradient thresholding with double threshold (100, 200) |
| Sobel Edge | Measures gradient in x and y directions separately, combines with sqrt(x²+y²) |
| Cartoonify | Bilateral filter for smooth colors + adaptive threshold for cartoon outline |
| Pencil Sketch | Dodge blend between grayscale and inverted blurred image |
| Emboss | Asymmetric kernel creates light/shadow effect simulating raised surface |
| Sepia | 3x3 matrix multiplication on RGB channels replicating vintage photograph look |
| Warm Tone | Boosts red channel, reduces blue channel |
| Cool Tone | Reduces red channel, boosts blue channel |
| Invert | Flips every pixel value (255 - value) |
| Background Blur | GrabCut foreground segmentation + Gaussian blur on background only |

---

## Requirements
All dependencies install automatically in the notebook:
- opencv-python-headless
- ipywidgets
- numpy
- matplotlib

---

## Tags
[opencv](https://github.com/topics/opencv) [image-processing](https://github.com/topics/image-processing) [python](https://github.com/topics/python) [colab](https://github.com/topics/colab) [ipywidgets](https://github.com/topics/ipywidgets)
