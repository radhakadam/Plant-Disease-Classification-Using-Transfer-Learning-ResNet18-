# Plant-Disease-Classification-Using-Transfer-Learning-ResNet18-
This project uses a convolutional neural network (CNN) with transfer learning (ResNet18) to classify plant leaf diseases from the PlantVillage dataset. It aims to assist farmers and agronomists in early identification of diseases in tomato, potato, and bell pepper plants.


Dataset: PlantVillage

Source: PlantVillage Dataset (kaggle)

Structure: 15 disease categories + 3 healthy categories

Image Types: RGB images of plant leaves in .jpg, .jpeg, or .png formats.


Example classes:

Tomato_Bacterial_spot

Tomato_Leaf_Mold

Tomato__Tomato_YellowLeaf__Curl_Virus

Potato___Early_blight

Pepper__bell___Bacterial_spot

Tomato_healthy, etc.

Each class contains 150–3000 images of leaves.



Workflow Summary:
🔹 1. Data Preparation
Dataset originally flat (one folder per class)

Split into train/ and val/ with 80/20 ratio

Used only .jpg, .jpeg, .png formats

🔹 2. Transformations
Train: Random crop, flip, tensor conversion

Validation: Resize, center crop, tensor conversion

🔹 3. Model Architecture
Based on ResNet18 (pretrained on ImageNet)

Final layer modified to fit number of classes

🔹 4. Training
Optimizer: SGD with momentum

Loss: CrossEntropyLoss

Epochs: 5 (can be increased)

Best model saved based on validation accuracy

🔹 5. Evaluation
Accuracy per epoch for both train and validation

Optional visualization of predictions



