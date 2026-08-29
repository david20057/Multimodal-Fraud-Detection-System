# Multimodal Fraud Detection System

## Overview

A Master's practicum project focused on detecting fraudulent and misleading online marketplace listings using multimodal artificial intelligence. The project investigates three complementary signals: image authenticity, text authenticity, and semantic consistency between product images and descriptions.

The proposed framework combines AI-generated image detection, AI-generated text detection, image-text consistency analysis, anomaly detection, and multimodal decision-level fusion to identify suspicious marketplace listings and support trust and safety in digital marketplaces.

## Technologies & Methods Used

* Python
* PyTorch
* CLIP (ViT-B/32)
* Pandas
* NumPy
* Scikit-learn
* Machine Learning
* One-Class SVM
* Isolation Forest
* NPR Deepfake Detection
* SAFE
* Binoculars
* Cosine Similarity
* Multimodal Decision-Level Fusion

## Key Features

* Analysed semantic consistency between product images and textual information using CLIP embeddings and cosine similarity.
* Developed a custom marketplace fraud dataset containing genuine and deliberately manipulated image-text listings.
* Evaluated supervised and unsupervised machine learning approaches for identifying anomalous marketplace listings.
* Compared One-Class SVM and Isolation Forest for anomaly detection using multimodal CLIP representations.
* Investigated domain-specific CLIP fine-tuning using visually similar smartphone products.
* Evaluated multiple AI-generated image detectors, including NPR Deepfake, SAFE, PatchCraft, and FreqNet.
* Evaluated AI-generated text detection methods, including Binoculars, RoBERTa models, and FastDetectGPT.
* Combined image authenticity, text authenticity, and semantic consistency signals using multimodal decision-level fusion.

## Datasets

The project used both publicly available and custom-built datasets, including:

* Amazon Berkeley Objects (ABO) dataset for genuine marketplace listings.
* Custom marketplace fraud dataset containing genuine and manipulated image-text pairs.
* Smartphone dataset for CLIP fine-tuning experiments.
* Custom dataset containing genuine and AI-generated product images.
* Custom dataset containing human-written and AI-generated marketplace descriptions.
* CNNDetection benchmark for evaluating the generalisation of AI-image detectors.

## Results

### Semantic Image-Text Consistency

CLIP-based semantic consistency analysis achieved:

* **84.45% accuracy**
* **79.52% precision**
* **92.80% recall**
* **85.65% F1-score**
* **94.80% ROC-AUC**

The results demonstrated that image-text consistency can provide a useful signal for identifying misleading marketplace listings.

### Anomaly Detection

One-Class SVM consistently assigned higher normality scores to genuine listings than fraudulent listings and achieved greater separation than Isolation Forest.

However, overlap between genuine and fraudulent samples showed that anomaly detection alone was insufficient for reliably identifying all fraudulent listings.

### CLIP Fine-Tuning

Domain-specific fine-tuning was investigated using visually similar smartphone products.

The fine-tuned model achieved higher recall but substantially lower accuracy and precision than the original CLIP model. The experiment showed that fine-tuning changed the model's behaviour but did not provide a substantial overall performance improvement.

### AI-Generated Image Detection

NPR Deepfake achieved the strongest performance on the custom marketplace image dataset:

* **99.50% accuracy**
* **99.01% precision**
* **100% recall**
* **99.50% F1-score**

SAFE achieved **97.00% accuracy** on the custom marketplace dataset and demonstrated stronger generalisation on the CNNDetection benchmark.

### AI-Generated Text Detection

Binoculars achieved the strongest overall performance among the evaluated AI-text detectors:

* **65.00% accuracy**
* **60.27% precision**
* **88.00% recall**
* **71.54% F1-score**

The results showed that AI-generated text detection was substantially more challenging than AI-generated image detection for marketplace content.

### Multimodal Fusion

The multimodal majority-vote framework achieved:

* **98.00% accuracy** when AI-generated images were paired with human-written descriptions.
* **98.50% accuracy** when AI-generated images were paired with AI-generated descriptions.

Although multimodal fusion achieved strong performance, NPR Deepfake alone achieved **99.50% accuracy** and remained the strongest individual detector.

The results therefore showed that image authenticity was the dominant signal for detecting synthetic marketplace listings, while multimodal fusion provided a structured approach for combining complementary evidence.

## Conclusion

The project demonstrates the potential of combining image authenticity, text authenticity, and semantic image-text consistency within a unified framework for marketplace fraud detection.

While multimodal fusion did not consistently outperform the strongest individual image detector, the framework provides a flexible foundation for future marketplace moderation systems capable of incorporating multiple forms of fraud evidence.

## Future Improvements

* Evaluate the framework on larger and more diverse real-world marketplace datasets.
* Investigate additional image and text authenticity detection models.
* Develop more advanced fusion strategies that dynamically weight different modalities.
* Incorporate seller history and behavioural information.
* Add pricing anomaly detection and additional marketplace metadata.
* Explore deployment within real-world marketplace moderation systems.
