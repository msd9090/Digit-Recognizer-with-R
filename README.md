
## 🔢 Digit Recognizer: High-Performance CNN in RThis repository contains a high-accuracy solution for the MNIST handwritten digit classification challenge. Using R and the Keras/TensorFlow framework, I implemented a deep Convolutional Neural Network (CNN) that achieves 99.2% accuracy through advanced regularization and architectural optimization.
## 🎨 1. Concept: How the AI "Sees"For those without a coding background,
think of this project as teaching a computer how to read.The Vision: We turn a $28 \times 28$ pixel image into a grid of numbers.The Brain: The "Neural Network" is a series of filters. The first filters see simple lines; the deeper filters see curves and loops; the final layer recognizes the whole number.The Test: After studying 42,000 examples, the model is tested on numbers it has never seen before to prove it truly understands handwriting.
## 💻 2. Technical ArchitectureThe model uses a Sequential CNN architecture designed to minimize error while preventing overfitting:
LayerConfigurationPurposeInput$28 \times 28 \times 1$Grayscale pixel values normalized to $[0, 1]$Convolution2x 32 filters (3x3)Extracting low-level spatial featuresBatch NormStandardAccelerates training and stabilizes gradientsMax Pooling$2 \times 2$Dimensionality reductionDropout25%Regularization to prevent "memorization"Convolution2x 64 filters (3x3)Extracting complex geometric patternsDense256 units (ReLU)High-level feature integrationOutput10 units (Softmax)Probability distribution for digits 0-9
## 📊 3. Performance & ResultsThe model demonstrates excellent convergence with minimal gap between training and validation scores.
Validation Accuracy: 99.21%Final Loss: 0.029
## 🚀 4. How to Run (Local Setup)PrerequisitesEnsure you have R and RStudio installed. 
You will also need a Python environment for the Keras backend (RStudio handles this automatically).Step 1: Install LibrariesRun the following in your R console:Rinstall.packages(c("tidyverse", "keras", "tensorflow", "readr", "abind"))

# Setup the AI engine
library(keras)
install_keras()
## Step 2: Prepare the DataDownload the dataset from Kaggle.Place train.csv and test.csv in the project root folder.Step 3: ExecuteOpen notebook-my-pred-2.ipynb in RStudio and click Run All. The script will:Preprocess and reshape the data.Train the CNN model.Generate a submission.csv file for Kaggle.
## 📂 5. Repository Structurenotebook-my-pred-2.ipynb: The complete end-to-end pipeline.submission.csv: Final predictions on the test set./images: Visualizations of data distribution and architecture.
## 🤝 6. ContributingIf you have suggestions for improving the architecture (e.g., adding Data Augmentation), 
feel free to open a Pull Request!Star this repo if you find it helpful! 
## ⭐Created by [mahmoud saad] [msd9090]
