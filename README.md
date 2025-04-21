# Recognizing-Handwritten-Alphabets
Handwritten Alphabet Classification Using Machine Learning
This project demonstrates a machine learning pipeline for classifying handwritten English alphabets (A–Z) based on image data. The goal was to evaluate multiple classification algorithms and identify the most effective model for this task.

Overview
The dataset used contains over 370,000 grayscale images of handwritten letters, organized into folders corresponding to each character. The project includes:

Data loading and preprocessing

Image resizing and flattening

Creation of a labeled DataFrame

Training multiple classification algorithms

Evaluating performance using accuracy

Dataset and Preprocessing
Source: Images were accessed from Google Drive via Colab.

Total Images: 372,451

Original Image Size: 28x28 pixels

Resized Image Size: 15x15 pixels (to reduce dimensionality and speed up processing)

Preprocessing Steps:
Loaded and resized all images to 15x15 using Pillow's thumbnail() method.

Flattened each image into a 1D array.

Created a labeled Pandas DataFrame from the flattened arrays.

Saved the final dataset to CSV (letters.csv).

Exploratory Data Analysis
Visualized the distribution of letter labels using count plots.

Randomly selected images were displayed to verify correctness after resizing.

Checked for label imbalance, revealing that some letters (e.g., 'O', 'S', 'U') were overrepresented, while others (e.g., 'I', 'F') were underrepresented.

Model Training and Evaluation
Features and Labels
X: Pixel values (15x15 = 225 features per image)

y: Corresponding letter labels (A–Z)

Train-Test Split
75% training data

25% testing data

Classifiers Used and Their Accuracy

Algorithm	Type	Accuracy
Logistic Regression	Linear Model	35.6%
Decision Tree Classifier	Tree-Based	92.8%
Random Forest Classifier	Ensemble	97.7%
AdaBoost Classifier	Boosting	53.8%
Bagging Classifier	Ensemble (Bagging)	95.4%
Insights and Observations
Random Forest Classifier outperformed all other models with an accuracy of 97.7%, making it the most suitable choice for this task.

Bagging Classifier also showed strong performance, achieving over 95% accuracy.

Decision Tree Classifier performed well but slightly under the ensemble models.

Logistic Regression and AdaBoost struggled with this high-dimensional, multi-class classification problem, likely due to the complexity of the image features.

Conclusion
The project demonstrates that ensemble learning methods, especially Random Forests, are highly effective in handling high-dimensional image classification tasks. While simple models like Logistic Regression fall short, more sophisticated approaches significantly improve performance.

Future Improvements
Experiment with Convolutional Neural Networks (CNNs) for more nuanced feature extraction.

Apply data normalization or pixel intensity scaling.

Use data augmentation to balance class distribution.

Perform hyperparameter tuning for all models to optimize performance.

Dependencies
This project was developed in Google Colab and requires the following libraries:

numpy

pandas

seaborn

matplotlib

scikit-learn

pillow (PIL)
