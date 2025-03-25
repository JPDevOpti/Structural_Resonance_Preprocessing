# 🧠 Structural Resonance Preprocessing 🧠

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![License](https://img.shields.io/badge/License-MIT-green)
![FSL](https://img.shields.io/badge/FSL-6.0.3-orange)

This repository contains a preprocessing pipeline for structural magnetic resonance imaging (MRI) data. The code allows for normalization, filtering, enhancement, and skull stripping of medical images in NIfTI format.

---

## 🚀 **Key Features**

1. **Image Comparison**: Visualize two MRI images side by side in coronal, axial, and sagittal slices.
2. **Intensity Normalization**: Adjust the intensity range of the image to improve contrast.
3. **Image Filtering**:
    - Median filter for noise reduction.
    - Gaussian filter for smoothing.
4. **Edge Enhancement**: Highlight edges of brain structures.
5. **Adaptive Histogram Equalization**: Improve local contrast using adaptive histogram equalization.
6. **Skull Stripping**: Remove non-brain tissues using FSL's BET (Brain Extraction Tool).
7. **Complete Pipeline**: Automatically process multiple patients with a single command.

---

## 📦 **Installation**

### Prerequisites

- Python 3.8 or higher.
- [FSL](https://fsl.fmrib.ox.ac.uk/fsl/fslwiki) installed and configured.
- Python libraries: `nibabel`, `matplotlib`, `scipy`, `scikit-image`.

### Install Dependencies

```bash
pip install nibabel matplotlib scipy scikit-image
```

---

## 🛠 **Usage**

### Processing a Single Patient

To process a single patient, run the following Python code:

```python
from preprocessing import process_patient

# Define the base directory and patient number
base_dir = '/path/to/your/directory'
patient_num = '023'

# Process the patient
process_patient(patient_num, base_dir, slice_index=100, show_comparisons=True, open_fsleyes=False)
```

### Full Pipeline

To process multiple patients, run the main script:

```bash
python main.py
```

---

## 🖼 **Visualization**

The code generates comparative visualizations at each step of the pipeline. Here's an example of what the images look like:

### Image Comparison

---

## 📂 **Project Structure**

```plaintext
Structural_Resonance_Preprocessing/
├── Images/
│   ├── 01_Images_Raw/          # Raw images
│   ├── 03_Images_Normalize/    # Normalized images
│   ├── 04_Images_MedianFilter/ # Median-filtered images
│   ├── 05_Images_GaussianFilter/ # Gaussian-filtered images
│   ├── 06_Images_HistogramEquialization/ # Histogram-equalized images
│   ├── 07_Images_EnhanceEdges/ # Edge-enhanced images
│   ├── 08_Images_Normalize_v2/ # Second-pass normalized images
│   └── 09_Images_SkullStripping/ # Skull-stripped images
├── Notebooks.py                # Main preprocessing code
│   ├── Preprocessing_Flow/     # Notebook with the process
├── main.py                     # Script to run the full pipeline
└── README.md                   # This file
```

---

## 🧩 **Main Functions**

```python
def compare_sRMI_images(nifti_path1, nifti_path2, slice_index):
     """Compare two MRI images in coronal, axial, and sagittal slices."""

def normalize_image(image_path, output_path):
     """Normalize the intensity of the image."""

def median_filter_image(image_path, output_path, size=3):
     """Apply a median filter to reduce noise."""

def apply_gaussian_filter(image_path, output_path, sigma=0.1):
     """Apply a Gaussian filter to smooth the image."""

def adaptive_histogram_equalization(image_path, output_path, clip_limit=0.01):
     """Improve local contrast using adaptive histogram equalization."""

def enhance_edges(image_path, output_path, weight=0.5):
     """Highlight edges of brain structures."""

def skull_stripping(input_image, output_image):
     """Perform skull stripping using FSL's BET."""

def process_patient(num_paciente, base_dir, slice_index=100, show_comparisons=True, open_fsleyes=False):
     """Process a single patient."""
```

---

## 🤝 **Contributions**

Contributions are welcome! If you have ideas to improve the code or add new features, please open an issue or submit a pull request.

---

## 📧 **Contact**

If you have questions or suggestions, feel free to reach out:

- **Name**: [Juan Pablo Restrepo Mancilla]
- **Email**: [juanpablorestrepo2020@gmail.com]
- **GitHub**: [PDevOpti]

Thank you for visiting this repository! 🎉

---

