# **Image Classification Using Genetic Algorithms and Random Forests**

This project implements an image classification model using genetic algorithms and a random forest classifier. The dataset is composed of images that represent various eye conditions, and the system uses genetic algorithms to optimize feature selection for improved accuracy.

## Dependencies
- numpy
- random
- time
- seaborn
- matplotlib
- scikit-learn
- keras

## How it Works
1. ### Data Preparation
The images are preprocessed using Keras' ImageDataGenerator, which resizes the images to a target size of 300x300 pixels, normalizes the pixel values, and splits the dataset into training, validation, and test sets.

2. ### Feature Selection with Genetic Algorithm
A genetic algorithm is used to optimize the feature selection process. The algorithm generates a population of candidate solutions (chromosomes), where each chromosome represents a subset of features. The population evolves through generations using crossover, mutation, and elitism, with the goal of selecting the most relevant features for the classification task.

3. ### Training the Random Forest Classifier
A random forest classifier is trained on the selected features. The classifier is evaluated using accuracy, precision, recall, F1 score, and specificity. Confusion matrices are visualized to assess the model's performance.

4. ### Evaluation and Results
The model's performance is evaluated on both the validation and test sets. Metrics are displayed, and misclassifications are highlighted in a grid of images for manual inspection. The training time and accuracy over generations are plotted for analysis.

## Key Functions:
**generate_data:** Preprocesses images and prepares the dataset.\
**fitness:** Evaluates the accuracy of a solution (chromosome).\
**mutate:** Applies mutation to a chromosome.\
**tournament_selection:** Selects the best individuals based on tournament selection.\
**uniform_crossover:** Combines two parent chromosomes to create a child chromosome.\
**evolve:** Evolves the population over multiple generations to optimize feature selection.\

## Model Evaluation:
After training, the model is tested using various metrics, including:
- Accuracy
- Precision
- Recall
- F1 Score
- Specificity

Confusion matrices and other visualizations are generated to evaluate performance and detect patterns in the classification errors.
