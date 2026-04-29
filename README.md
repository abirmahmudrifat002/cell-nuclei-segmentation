# 🔬 Cell Nuclei Segmentation — ML Project

## 📋 Course Information
| Field | Details |
|-------|---------|
| **Course** | CSE445 |
| **Section** | 6 |
| **Instructor** | Professor M. Shifat-E-Rabbi (MSRb) |
| **Group No.** | 2 |

---

## 👥 Group Members
| Name | Student ID |
|------|-----------|
| Abir Mahmood Rifat | 2132677642 |
| Mohammad Safayet Hossain Alif | 2232562642 |
| Md. Sahinul Islam Rizve | 2232504042 |
| Md. Muammer Faisal | 1410384042 |

---

## 📌 Project Overview
This project builds a deep learning model to automatically detect
and segment cell nuclei from microscopy images. Cell nuclei segmentation is a critical task in medical
image analysis, enabling automated detection of cells across
heterogeneous backgrounds.

---

## 🗂️ Dataset
| Field | Details |
|-------|---------|
| **Source** | 2018 Kaggle Data Science Bowl |
| **Original Images** | 10 whole slide images |
| **Backgrounds** | Heterogeneous (different types) |
| **After Augmentation** | ~40 images |
| **Image Size** | 128 x 128 pixels |

---

## 🧠 Model Architecture — U-Net
Input (128x128x3)
↓
Encoder (Conv + MaxPool) → learns features
↓
Bottleneck (deepest layer)
↓
Decoder (UpSampling + Conv) → rebuilds mask
↓
Output Mask (128x128x1)

---

## 📊 Results
| Metric | Score |
|--------|-------|
| **Metric Used** | IoU (Intersection over Union) |
| **Average IoU Score** |0.7381|
| **Best IoU Score** |0.8613|
| **Worst IoU Score** |0.5607|

---

## 🗂️ Project Structure
nuclei_segmentation/
├── images/                //raw dataset images(data)
├── masks/                
├── notebooks/          //support 
│   └── nuclei_project.ipynb
├── model/               
│   ├── nuclei_final_model.keras
│   ├── best_model_v?.keras
│   └── all_10_results.png
├── requirements.txt      
└── README.md             
