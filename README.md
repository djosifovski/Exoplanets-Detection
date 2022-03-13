# Exoplanets Detection

## Motivation

Exoplanets are planets that can be found outside the Solar System, i.e., they are revolving about other star. It is very difficult to detect planets that are many light years away from Earth because they are relatively small and are a lot fainter compared to the star they are revolving about. In 2009 NASA launched the Kepler space telescope to look for exoplanets. The motivation for this project is according to data collected by the space telescope of the astronomical objects to classify whether the object is an exoplanet or not. This could be another tool that astronomers use to verify if they have observed a new exoplanet.

## Methodology

This is a binary classification type of problem in which a subset of learning algoritms were trained from `scikit-learn`, and stacking classifier with cross-validation from `mlxtend`. As a single number evaluation metric F_1 is used, and after fine-tuning the models, the most optimal model is Random Forest where F_1=0.996860.

It turned out that the candidates set has a somewhat different distribution than the train, validation and test sets, and Random Forest isn't powerful enough to predict correctly. To mitigate this problem, an artificial neural network was built using `TensorFlow` framework which gave much more promising results.