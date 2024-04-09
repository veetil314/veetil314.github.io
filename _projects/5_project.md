---
layout: page
title: Bridging the Gap Between Image Content and Product Intelligence
description: DeepView.ai's Fashion Search Technology
img:
importance: 4
category: work
---


# Bridging the Gap Between Image Content and Product Intelligence: DeepView.ai's Fashion Search Technology

## Executive Summary
DeepView.ai has developed a cutting-edge fashion search technology that addresses the disconnect between image content and product intelligence in the e-commerce industry. By leveraging advanced deep learning image recognition, DeepView.ai enables retailers to enhance product discovery on websites, apps, and social media platforms. This innovative solution has proven to increase conversions by up to 15% within just three weeks of deployment.

## Introduction
Search technology has made significant advancements, with users expecting near-perfect results. However, the e-commerce industry still faces challenges in providing relevant and comprehensive search results, particularly in the fashion domain. Retailers struggle to accurately annotate products with relevant keywords, leading to user frustration and suboptimal search experiences.

## The Problem
Fashion shoppers often have a specific look or style in mind when searching online. They translate this desired look into words and attempt to find relevant products on retail websites. However, two key challenges arise:

1. Translating the desired look into appropriate search terms can be difficult, as many patterns and styles lack clear names.
2. Products must be properly annotated with the words used by the user to appear in search results. Inaccurate or incomplete annotations lead to irrelevant or scarce search results.

## DeepView.ai's Solution
DeepView.ai addresses these challenges by leveraging advanced deep learning image recognition. The AI-powered solution enables retailers to:

1. **Index products with automatic, image-based SMART METADATA**: DeepView.ai's technology reduces the effort required for manual tagging by 80% and improves search results for underserved queries by 5x.

2. **Increase click-through rates on recommended products**: Visual image search enhances product recommendations, leading to higher click-through rates, even for out-of-stock products.

3. **Make user-generated and social media images automatically shoppable**: By matching user-generated content (UGC) and social media images with similar products in the online store, DeepView.ai enables retailers to capitalize on the power of visual content.

4. **Generate automatic hashtags for social media images and improve SEO**: DeepView.ai's technology automatically generates relevant hashtags for social media images, enhancing discoverability and improving search engine optimization (SEO).


## Technology 
-----------------------------

### Data Collection

Limited video data was provided by the client for training, which we supplemented with data extracted from various public sources. Our team curated and extracted web video data. Street style images are very difficult to train on due to various conditions:

1. **Pose Variations**: Wearers may be in different poses, such as sitting or standing. Clothing may not be worn and could be shown as folded or hanging from a wardrobe. These pose variations introduce complexity in recognizing fashion items accurately.

2. **Occlusion**: Cluttered backgrounds and partial occlusion of fashion items are common in street style images. This makes it challenging for the model to identify and isolate the relevant fashion elements.

3. **Lighting Conditions**: Fashion is highly sensitive to lighting. Color pixels can change substantially under different lighting conditions, making it difficult to recognize and match fashion items consistently.

4. **Attribute Sensitivity**: Fashion search involves multiple attributes that need to match. For example, when searching for a mini dress, users may be looking for specific characteristics such as the shape (e.g., bodycon), sleeve length (e.g., sleeveless, half sleeve, or full sleeve), neckline (e.g., sweetheart, round, or V-neckline), pattern, color, etc. Matching these attributes accurately is crucial for providing relevant search results. We found that generating specific data for each attribute was necessary to train the model effectively.

To address these challenges, we employed various techniques during data collection and preprocessing, such as data augmentation, image normalization, and attribute-specific data generation.

### Data Annotation

We recruited an in-house team of annotators for this project. Developing clear guidelines for the team proved challenging, necessitating an iterative process that included an evaluation phase. During this phase, we continuously refined the guidelines. Annotators were only approved for production annotation after achieving satisfactory accuracy levels in the evaluation phase.

Annotation requirements were extensive. The work encompassed various models, including fashion item detection and classification of various attributes. The diversity of data was also critical. Data was categorized based on various sources to ensure diversity at every level. For instance, stock videos are generally cleaner, whereas YouTube videos are noisier. Longer videos were not overrepresented to avoid repetitive occurrences of similar images within the dataset.

At that time, there were no suitable annotation tools available, so we built our own in-house tagging tool. This tool was hosted on AWS, providing a scalable and accessible platform for our annotation team.

First, a baseline model was trained purely based on taxonomy. This model was used to initially train triplet loss. Then, hard positive and negative triplets were generated iteratively. These triplets were manually tagged by annotators and fed back into the system. This approach greatly sped up the annotation process and improved the model's performance.

### Active Learning

Active learning strategies were employed to minimize annotation requirements. Models would automatically annotate samples, and only corrections made by annotators were required. This greatly improved annotation speed and reduced the manual effort involved in the annotation process.

### Image Augmentation

To address the need to handle various technical challenges, including clutter, occlusion, diverse lighting & camera angles, and diversity of clothing, we performed extensive data augmentation. This involved applying techniques such as random cropping, flipping, rotation, and color jittering to the images. Data augmentation helped in increasing the variability and robustness of the training data, enabling the model to learn more generalized features.

### Model Development

1. **Object Detection**: Accurate object detection was critical for fashion search. We trained separate detectors for major categories such as tops, skirts, dresses, outerwear, etc. These categories had enough shape differences to warrant separate detectors, improving the overall accuracy of the system.

2. **Siamese Architecture**: Initially, we experimented with a Siamese architecture for fashion similarity matching. However, this approach did not produce sufficiently accurate results. We realized that fashion similarity required a more nuanced understanding of various attributes.

3. **Triplet Loss**: We found that using triplet loss worked better for fashion similarity matching. Triplet loss allows the model to learn a metric space where similar fashion items are closer together, and dissimilar items are farther apart. This approach improved the model's ability to match fashion items accurately.

4. **Joint Training**: To further enhance the accuracy of the fashion search model, we employed joint training. We jointly trained classifiers for various attributes alongside the triplet loss minimization. This approach allowed the model to learn both the attribute-specific features and the overall similarity metric simultaneously.

5. **Rich Taxonomy**: We utilized a rich taxonomy of fashion objects to capture the diverse characteristics of fashion items. This taxonomy included attributes such as:
  - Sleeve length: sleeveless, half sleeve, ¾ sleeve, full sleeve
  - Neckline: round neck, cowl neck, V-neck, sweetheart neckline
  - Pattern: jacquard, paisley, and more
  - Shape: bodycon dress, sheath dress, shift dress, A-line dress, and similar categories for skirts, tops, etc.

By jointly training classifiers for these attributes and the triplet loss minimization, we achieved the best accuracy for fashion search. The combination of attribute-specific features and the overall similarity metric allowed the model to understand the nuances of fashion and provide highly relevant search results.

The development of our fashion search technology involved extensive data collection, annotation, active learning, image augmentation, and iterative model development. By addressing the unique challenges posed by street style images and leveraging advanced techniques such as triplet loss and joint training, we were able to create a highly accurate and efficient fashion search system.

## Differentiating Factors
DeepView.ai's solution stands out from competitors in two key aspects:

1. **Natural image compatibility**: The technology works seamlessly with natural images, social media content, and UGC, unlike most image recognition APIs that struggle with noisy or non-professional images.

2. **Product-specific feature generation**: DeepView.ai's system generates product-specific features based on images, rather than generic tags that are irrelevant for search purposes.

## Demos
To showcase the capabilities of DeepView.ai's fashion search technology, we invite you to watch the following demo videos:

- [Demo 1](https://www.youtube.com/watch?v=P2nkm4QQ4OM)
- [Demo 2](https://www.youtube.com/watch?v=q4-2MX2ijJE)

## Conclusion
DeepView.ai's fashion search technology revolutionizes the e-commerce industry by bridging the gap between image content and product intelligence. By leveraging advanced deep learning image recognition, retailers can significantly enhance product discovery, increase conversions, and improve the overall user experience. With a proven track record of delivering results within a short timeframe, DeepView.ai is poised to transform the way consumers shop for fashion online.