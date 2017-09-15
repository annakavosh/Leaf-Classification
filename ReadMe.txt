
There are estimated to be nearly half a million species of plant in the world. Classification of species has been historically problematic and often results in duplicate identifications. Automating plant recognition might have many applications, including:

Species population tracking and preservation
Plant-based medicinal research
Crop and food supply management


Data Introduction:


The dataset consists approximately 1,584 images of leaf specimens (16 samples each of 99 species) which have been converted to binary black leaves against white backgrounds. Three sets of features are also provided per image: a shape contiguous descriptor, an interior texture histogram, and a ﬁne-scale margin histogram. For each feature, a 64-attribute vector is given per leaf sample.


My code for Leaf Identification Kaggle:


I will use four different models from a very basic level up to GridSearch, using only the pre_extracted features. Then I will use Dense Neural Network(DNN) again using the pre_extracetd features. At the end I will use Convolutional Neural Networks to classify grey-scale images (along with pre-extracted features) to identify each image as one of 99 leaf species.
CNN models will either incorporate multiple convolutional layers as well as merging the features extracted by the convolutions with a pre-extracted feature set (provided by Kaggle) of each leaf image. Each model will be evaluated by minimizing the loss function, log-loss.


File descriptions

train.csv - the training set
test.csv - the test set
sample_submission.csv - a sample submission file in the correct format
images - the image files (each image is named with its corresponding id)
Data fields

id - an anonymous id unique to an image
margin_1, margin_2, margin_3, ..., margin_64 - each of the 64 attribute vectors for the margin feature
shape_1, shape_2, shape_3, ..., shape_64 - each of the 64 attribute vectors for the shape feature
texture_1, texture_2, texture_3, ..., texture_64 - each of the 64 attribute vectors for the texture feature