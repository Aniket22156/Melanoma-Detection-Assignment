
# Melanoma Detection Using CNN

This project focuses on building a robust Convolutional Neural Network (CNN) model capable of accurately detecting melanoma, a deadly form of skin cancer responsible for 75% of skin cancer-related deaths. By automating the image evaluation process, the solution aims to assist dermatologists in early detection, reducing manual effort and improving diagnosis accuracy.

# Business Challenge:

The core objective is to streamline the detection of melanoma using image analysis. The dataset used for this project includes 2,357 images of both malignant and benign skin conditions sourced from the International Skin Imaging Collaboration (ISIC). The diseases represented include:

	•	Actinic keratosis
	•	Basal cell carcinoma
	•	Dermatofibroma
	•	Melanoma
	•	Nevus
	•	Pigmented benign keratosis
	•	Seborrheic keratosis
	•	Squamous cell carcinoma
	•	Vascular lesion

# Conclusions:

## Model 1: Initial Approach

	•	Input: Images with dimensions (180, 180, 3)
	•	Architecture:
	•	Two convolutional layers with 32 filters (3x3) and same padding, followed by max-pooling.
	•	Additional convolutional layers with 32 and 64 filters (3x3), followed by max-pooling.
	•	Fully connected layer with a softmax function to classify images into 9 categories.
	•	ReLU activation is applied throughout for computational efficiency and to prevent vanishing gradient issues.
	•	Key Observations:
	•	Training accuracy reached 69%, while validation accuracy was 51%, highlighting significant overfitting.
	•	Training accuracy improves with more epochs, but validation accuracy plateaus or declines.
	•	After 10 epochs, validation loss increases while training loss continues to decrease.

## Model Revision: Data Augmentation

	•	Problem: The dataset was imbalanced, with some classes like seborrheic keratosis having only 77 images, while others had significantly more.
	•	Solution: Data Augmentation was applied to balance the dataset by increasing the number of samples in underrepresented categories.
	•	Observations:
	•	Training accuracy decreased to 52% and validation accuracy to 53%, but overfitting was resolved as both accuracies followed similar trends.
	•	However, overall accuracy still needed improvement.

## Model 3: Final Iteration with Augmentor

	•	Enhancement: Additional images were generated, increasing each class by 500+ samples to achieve a more balanced dataset.
	•	Final Model Performance:
	•	Test accuracy improved to 90%, and validation accuracy to 80%.
	•	Although further epochs led to overfitting, the model’s performance improved significantly once class imbalance was addressed.

# Technologies Used:

	•	Google Colab
	•	Python
	•	TensorFlow

