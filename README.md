# Multimodal Fraud Detection System

## Overview

A master's practicum project focused on detecting fraudulent and misleading e-commerce listings by analysing product images and textual content. The project investigated multimodal machine learning techniques, image-text consistency, anomaly detection, and content authenticity to identify suspicious listings and improve trust and safety within online marketplaces.

## Technologies Used

* Python
* PyTorch
* CLIP
* Pandas
* NumPy
* Scikit-learn
* OpenCV
* Machine Learning

## Key Features

* Generated image and text embeddings using CLIP to measure consistency between product images and listing descriptions.
* Applied cosine similarity and anomaly detection techniques to identify potentially misleading listings.
* Analysed image authenticity to help identify manipulated, stolen, or AI-generated product images.
* Combined multiple detection signals to improve overall fraud classification performance.
* Evaluated model performance using manually labelled real and fraudulent marketplace listings.

## Results

The system demonstrated strong performance across several fraud detection components. CLIP-based image-text analysis achieved approximately 96.5% accuracy, while image authenticity approaches achieved up to 99.5%. Combining multiple detection signals produced overall performance of up to 98.5%.

The results demonstrated the potential of combining textual, visual, and authenticity signals to detect suspicious e-commerce listings more effectively than relying on a single detection method.

## Future Improvements

* Expand the dataset with a larger and more diverse collection of marketplace listings.
* Improve detection of AI-generated and manipulated product images.
* Explore additional multimodal and transformer-based models.
* Integrate the detection system into a real-world marketplace platform.
* Develop real-time fraud scoring for newly submitted listings.
