# Half U-Net for Eye Segmentation

## Project Description
This project presents an improved eye segmentation model using Half U-Net, achieving **89.6% Intersection over Union (IoU)** and **87.4% Dice Coefficient**. The model was enhanced by experimenting with customized loss functions such as **Dice Loss, Binary Cross-Entropy (BCE), Hybrid Loss, and K-Loss** to optimize performance.

## Project Structure
```
.
├── Half_Unet_Eye.ipynb            # Jupyter Notebook with model implementation
├── Results                         # Folder containing model results, predictions, and metrics
├── Dataset                         # Dataset structure
│   ├── nil_files/                  # Input data (X)
│   └── labels/                     # Corresponding masks (Y)
```

## Dataset Information
The dataset consists of labeled eye images where each pixel belongs to specific anatomical structures, such as:
- **Iris**
- **Pupil**
- **Sclera**

The data is in **NIfTI (.nii)** format, which is commonly used in medical imaging applications. The segmentation masks provide pixel-wise annotations for training the model.

## Implementation Steps
### 1. Install Required Dependencies
Ensure you have Python **3.10** installed. First, check if `pip` is installed:
```bash
pip --version
```
If not installed, upgrade it:
```bash
python3.10 -m pip install --upgrade pip
```
Next, install all required dependencies using:
```bash
pip install -r requirements.txt
```

### 2. Setting Up the Dataset
Organize the dataset as mentioned in the **Project Structure**. If the dataset is unavailable, the script will automatically download it.

### 3. Running the Model
Execute the Jupyter Notebook:
```bash
jupyter notebook
```
Open **Half_Unet_Eye.ipynb** and run all the cells to train and evaluate the model.

---

## Half U-Net Architecture
Half U-Net is a lightweight version of the standard **U-Net**, optimized for efficiency without significant loss in accuracy.

### Key Features of Half U-Net:
- **Unification of Channel Numbers:**
  - Standardizes channel dimensions to reduce computational overhead.
- **Full-Scale Feature Fusion:**
  - Merges multi-scale features, ensuring both fine and coarse details are captured.
- **Ghost Modules:**
  - Reduces parameter count and floating-point operations (FLOPs) while maintaining performance.

### Advantages of Half U-Net:
- **Reduced Computational Complexity:**
  - **98.6% fewer parameters** than the standard U-Net.
  - **81.8% fewer floating-point operations.**
- **Comparable Accuracy to U-Net Variants** across multiple medical imaging tasks, such as:
  - Mammography segmentation
  - Lung nodule segmentation (CT images)
  - Left ventricular segmentation (MRI images)

---

## Loss Functions Used
To improve segmentation performance, the model was trained with multiple loss functions:

1. **Dice Loss:** Measures the overlap between predicted and ground truth masks.
2. **Binary Cross-Entropy (BCE):** Standard loss for binary segmentation problems.
3. **Hybrid Loss (Dice + BCE):** Combines the benefits of both loss functions.
4. **K-Loss:** A custom loss function designed for improved segmentation accuracy.

These loss functions were evaluated to determine the most effective optimization strategy for eye segmentation.

---

## Conclusion
Half U-Net provides an efficient and accurate solution for medical image segmentation. The model achieves high segmentation performance while significantly reducing computational costs, making it ideal for real-time and resource-constrained applications.

---

### Author
**Sai Krishna Chowdary Chundru**

For further queries, feel free to contact:
- **Email:** cchsaikrishnachowdary@gmail.com
- **LinkedIn:** linkedin(https://linkedin.com/in/sai-krishna-chowdary-chundru)
- **GitHub:** [github.com/sAI-2025](https://github.com/sAI-2025)

