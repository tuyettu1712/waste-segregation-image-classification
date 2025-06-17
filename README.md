WASTE SEGREGATION PROJECT
CNN IMAGE CLASSIFICATION MODEL
By Tuyet Tu

=======PROBLEM STATEMENT=======
Improper waste disposal contributes to environmental degradation, increased landfill waste and inefficient recycling processes. Manual sorting is labour-intensive, error-prone and costly. An AI-powered waste classification system addresses these challenges by streamlining waste segregation, reducing operational costs and improving recycling rates.

=======OBJECTIVE=======
The objective of this project is to implement an effective waste material segregation system using convolutional neural networks (CNNs) that categorises waste into distinct groups. This process enhances recycling efficiency, minimises environmental pollution, and promotes sustainable waste management practices.

Key goals:
* Accurately classify waste materials into categories like cardboard, glass, paper, and plastic
* Improve waste segregation efficiency to support recycling and reduce landfill waste
* Understand the properties of different waste materials to optimise sorting methods for sustainability

=======DATASET OVERVIEW=======
Total Images: 7,625 waste images across 7 categories
Image Format: PNG files (256×256 pixels, RGB)

Data Distribution:
- Plastic: 2,295 images (30.1%)
- Paper: 1,030 images (13.5%)
- Other: 1,010 images (13.2%)
- Food Waste: 1,000 images (13.1%)
- Metal: 1,000 images (13.1%)
- Glass: 750 images (9.8%)
- Cardboard: 540 images (7.1%)

Data Preprocessing:
- Image resizing to 224×224 pixels
- Pixel normalization to [0,1] range
- One-hot encoding for labels
- 70-30 stratified train-validation split

=======MODEL ARCHITECTURE=======
Final Model: 4-layer CNN with class weights
Total Parameters: 456,007
Optimization: Adam optimizer with categorical crossentropy loss

Training Features:
- Class weights to handle imbalanced dataset
- EarlyStopping with patience=7
- ModelCheckpoint for best model saving
- ReduceLROnPlateau with factor=0.7

=======PERFORMANCE RESULTS=======

Model Performance:
- Accuracy: 55.5%
- Precision: 56.0%
- Recall: 55.5%
- F1 Score: 55.3%

Key Findings:
- 4-layer architecture provides optimal performance-efficiency balance
- Class weights improved validation accuracy by 2.3%
- Strong performance on majority classes (Plastic, Paper)
- Room for improvement on minority classes (Glass, Cardboard)

=======REQUIREMENTS=======
Python: 3.10.18
Dependencies:
- numpy: 1.26.4
- pandas: 2.2.2
- seaborn: 0.13.2
- matplotlib: 3.10.0
- PIL: 11.1.0
- tensorflow: 2.18.0
- keras: 3.8.0
- sklearn: 1.6.1
