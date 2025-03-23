# 3D Pose Estimation

This project focuses on person re-identification (ReID), a crucial task in computer vision where a person must be recognized across different frames and camera viewpoints. The goal is to extract a feature vector from a bounding box to ensure reliable matching.

## 📌 Features
- **Feature Extraction**: Generates feature vectors from person images.
- **Multi-frame Matching**: Matches individuals across different frames.
- **Deep Learning-based**: Utilizes deep learning models for improved accuracy.

<!--## 📂 Project Structure-->
<!--```plaintext-->
<!--/final.ipynb        # Main Jupyter Notebook-->
<!--/data               # Dataset directory (if applicable)-->
<!--/models             # Pre-trained or trained models-->
<!--/outputs            # Results and evaluation outputs-->
<!--```-->
### 🔹 Pose Estimation
1. **YOLO Model** for effective pose estimation and tracking.
2. Extracting keypoints and bounding boxes.
### 🔹 ReID Approach
1. **Bounding Box Detection**: A person is detected using an object detection model like **YOLO**.
2. **Feature Extraction**: A deep learning model (FastReID) extracts a **feature vector** that represents the person uniquely.
3. **Metric Learning**: The extracted feature vectors are compared using a **distance metric** (e.g., cosine similarity, Euclidean distance).
4. **Re-Identification**: The system matches individuals across different frames based on similarity scores.
5. Maintaining a database to effectively store feature vectors and identity of unique people.

### 🔹 Triangulation Approach
1. Using projection matrics, extrinsic and intrinsic properties of camera to triangulate and get corresponding 3D points.
2. Using these 3D points to create skeleton of player.
3. We used weighted moving averages to smoothen out 3D pose estimation throughout the frames.
4. Re-verifying the ids assigned by ReID model to further validate the estimation.

<!--## 🔧 Technologies Used-->
<!--### 📌 Deep Learning & Machine Learning-->

## 🚀 Installation & Usage
### 1️⃣ Clone the Repository
```sh
git clone https://github.com/harshitkapoor03/3D_Pose_estimation.git
cd 3D_Pose_estimation
```
<!--### 2️⃣ Install Dependencies-->
<!--```sh-->
<!--pip install -r requirements.txt-->
<!--```-->
### 2️⃣ Run the Notebook
Open and execute `final.ipynb` using Jupyter Notebook or Jupyter Lab.

<!--## 📊 Results-->
<!--- Evaluation metrics such as Rank-1 accuracy and mAP.-->
<!--- Visualization of re-identification matches.-->

## 🔍 Future Work
- Improving similarity and loss functions to effectively differentiate between persons.
- Enhancing robustness in occlusions and varied lighting.
- Improving ReID by using 3D field modelling.
- Applying threading and other parallel processing technuiques to achieve almost real time detection and re-identification.

## 📜 License
This project is licensed under the MIT License.

<!------->

<!--👤 **Author**: [Your Name]  -->
<!--📧 Contact: your.email@example.com  -->
