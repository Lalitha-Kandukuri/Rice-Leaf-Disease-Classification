# 🌾 Rice Leaf Disease Classification  

Rice is one of the most important staple foods in the world, especially in low- and middle-income countries. Detecting rice leaf diseases early helps farmers reduce crop loss and improve yield.  

This project classifies rice leaf diseases into three categories:  
- 🍂 **Leaf Smut**  
- 🍃 **Brown Spot**  
- 🌱 **Bacterial Leaf Blight**  

---

## 📂 Dataset  
- Total: **120 images** (JPG format)  
- Classes: **3** (40 images each)  
- Classes split into **Train (75%)** and **Test (25%)**  

---

## ⚙️ Tech Stack  
- **Python, TensorFlow, Keras**  
- **MobileNetV2** (Pretrained Model with Transfer Learning)  
- **OpenCV, Matplotlib, NumPy, Pandas**  

---

## 🛠️ Steps Followed  

### 1️⃣ Data Preparation  
- Unzipped dataset and organized into folders  
- Split into train (75%) and test (25%) sets  

### 2️⃣ Data Augmentation  
- Applied rotation, zoom, shear, shift, and flip using `ImageDataGenerator`  
- Normalized images (`rescale=1/255`)  

### 3️⃣ Model Building  
- Used **MobileNetV2** as base model (transfer learning)  
- Added `GlobalAveragePooling2D`, `Dropout (0.5)`, and `Dense Softmax` layer (3 outputs)  

### 4️⃣ Compilation & Training  
- Loss: **Categorical Crossentropy**  
- Optimizer: **Adam (1e-4)**  
- Metric: **Accuracy**  
- Added **callback** to stop training after 98% accuracy  

### 5️⃣ Model Saving  
- Saved model as `model.h5`  
- Exported weights as `my_model_weights.h5`  

### 6️⃣ Testing & Evaluation  
- Loaded trained model  
- Tested with unseen images  
- ✅ Correctly predicted rice leaf disease class  

---

## 📊 Results  
- Achieved **high accuracy** on training & testing datasets  
- Successfully identified rice leaf diseases on new images  

---
