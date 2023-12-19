# NLP-Medical-Abstract-Segmentation-Using-TensorFlow

This repository contains code for performing medical abstract segmentation using TensorFlow. The process involves various steps from data acquisition, preprocessing, setting up multiple experiments with different embeddings, building models, replicating existing models, and finally, creating a tribrid embedding model.
## Getting Started
## Data Acquisition

Download the text data from PubMed 200K RCT dataset (link to dataset).
## Preprocessing

A set of preprocessing functions has been developed to clean and prepare the text data for model training. These functions handle tasks such as tokenization, data cleaning, and feature extraction.
## Modelling Experiments

Multiple experiments with varying levels of embeddings have been set up to explore different embedding techniques and their impact on model performance.
## Building the Model
### Model Architecture

The model architecture is designed to incorporate different sources of data and replicate the functionality described in arXiv:1710.06071.

    Building token level models
    Creating character level models
    Developing models for 'line_number' and 'total_lines' features

### Combining Outputs

The outputs from the various models are combined using tf.keras.layers.concatenate to create integrated representations of the input data.
Tribrid Embeddings

The final model incorporates a tribrid embedding architecture, combining outputs from token level, character level, 'line_number,' and 'total_lines' models.
Output Layer

An output layer is designed to accept the tribrid embeddings and generate label probabilities.
Overall Model

All the input and output components are combined using tf.keras.Model to create the final model architecture.
Finding the Most Wrong Predictions

For model evaluation and analysis, a method to identify and analyze the most wrong predictions has been implemented. This helps in understanding model weaknesses and areas for improvement.
