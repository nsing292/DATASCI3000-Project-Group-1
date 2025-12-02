# DATASCI3000-Project-Group-1

Group 1: Nicholas Singh, Anderson McAlpine, Alex Hobson, Joe Bailey

**Purpose:**
Gear failure is a major source of downtime and financial loss in industrial and mechatronic systems. Traditional maintenance strategies often rely on reactive or scheduled replacement, which can miss early indicators of damage. This project focuses on developing a machine learning classification system that can identify different types of gear faults from vibration signals. By using multiple different learning models, we aim to develop an effective model that can detect the earliest signs of mechanical degradation. The goal is to improve reliability, reduce unplanned stoppages, and support predictive maintenance practices in smart manufacturing environments.

**Dataset:** https://www.kaggle.com/datasets/hieudaotrung/gear-vibration 
(“Mechanical Gear Vibration Dataset”) sourced from Kaggle contains time-series vibration signals collected under six conditions: No Fault, Eccentricity Fault, Missing Tooth, Root Crack, Surface Fault, Tooth Chipped Fault. Each CSV file records multiple vibration amplitude samples over time, measured at consistent sampling rates under controlled rotational speeds and loads. This structured dataset will allow the models to learn discriminative patterns between healthy and faulty gears.

Pre and post processing will include: Normalisation and scaling of amplitude values, Conversion of signals from times to frequencies, Extraction of statistical features (RMS, F1 score, accuracy, ROC, AUC), labelling each signal by fault type, Data inspection (check for outliers, null values, etc).

**Methodology:**
Project includes experimentation with both traditional and modern machine-learning techniques: The models will be evaluated using cross-validation on accuracy, precision, recall, and F1-score. Data will be split 70/15/15 for training, validation, and testing. Preliminary tests show clear separability in frequency spectra between healthy and defective gears, suggesting strong potential for accurate classification.

Baseline: K-Nearest Neighbours (KNN) and Support Vector Machine (SVM) using extracted time/frequency-domain features. These can help verify the effectiveness of the pre-processing and also help with nonlinear relations, which can then be applied to other models. 

Advanced: Random Forest and Gradient Boosting for non-linear decision boundaries, which effectively handle noisy data and ensure correct fitness.

Exploratory: 1-D Convolutional Neural Network (CNN) for direct time-series classification if data volume permits. Added bonus of handling the feature engineering on its own.

Running the Program: We developed this program in Google Colab. To recreate our results, please download all of the files provided in the github and upload them to your Google Drive. You need to ensure that your file path, which is defined as dataLocation = "/content/drive/MyDrive/DATASCI_3000_Project/Code" in the first cell. Match this to match your file path. If you do not wish to run this program on Colab, please remove the Google Drive mount and alter the file pathing so that the files can be accessed locally on your computer. For best results, please use Colab, as this is where we ran all of our testing. 

