---
layout: page
title: Heavy Equipment Monitoring with AI for Top 5 Construction Firm in Asia Pacific 
description: Reflective AI technology to measure heavy equipment activity in civil construction projects from video feeds for client.
img: assets/img/earthwork.jpg
importance: 4
category: work
giscus_comments: false
---

<h2>Project Overview</h2>
<p>With the goal of significantly enhancing efficiency in civil construction projects, our team at Reflective AI embarked on a mission to change the way heavy equipment is monitored and managed. Collaborating with one of the largest construction firms in the Asia Pacific region, we leveraged advanced AI-driven video recognition technology to accomplish this. The technology provides real-time, actionable insights into heavy equipment, beginning with dump truck operations, thereby addressing critical operational bottlenecks and enhancing overall project efficiency.
</p>

<h2>Problem</h2>
<p>
The initial digitization focus was on earthwork operations, with plans to expand to other areas, including building construction and manual operations. Earthwork is a substantial cost factor in large infrastructure projects, involving numerous trucks transporting materials, excavators performing cut and fill operations and more. Understanding and digitizing these operations was essential but challenging with traditional technologies including IoT sensors, due to the high turnover of independent equipment operators, leading to challenges in deep IoT integration. A camera-based solution emerged as an effective method to bypass these challenges, helping to eliminate bottlenecks, delays, and simplify integration.
</p>

<h2>Solution</h2>


<p>
We developed technology to intelligently recognize the fine-grained activity of heavy equipment, such as whether it's loaded/unloaded, counting the number of dumps, and distinguishing between moving and idle states. This approach offers a detailed overview of material movement, utilization, and productivity without requiring complex infrastructure. A few cameras covering the work area, necessary for security and monitoring, are used.

An easy-to-use UI generates a smart video summary that highlights key activities like dump truck activity.  Heatmaps are created to show areas of high activity over a day or fixed period of time , and metrics reveal the percentage of idle time, detailed equipment activity and the spatial distribution of activity.
</p>



## Key Technology Highlights

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.liquid path="https://vimeo.com/935174600" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Recognizing dump truck activity. Notice how a second noisy unload action to the right corner is also captured. 
</div>


[//]: # (This is also a comment using a non-standard but widely supported Markdown method)
[//]: # {% include video.liquid path="https://player.vimeo.com/video/935174600" class="img-fluid" width="100%" min-width="300px" caption="This is a descriptive caption for the video." %}
[//]: # <iframe src="https://player.vimeo.com/video/935174600?h=d022a0ccfe" width="640" height="564" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>

<div class="row"> 
  <div class="col-sm mt-3 mt-md-0"> 
        {% include video.liquid path="assets/video/youtube4.mp4" class="img-fluid rounded z-depth-1" controls=true autoplay=true %}
  </div> 
</div>
<div class="row"> 
  <div class="col-sm mt-3 mt-md-0"> 
        {% include video.liquid path="assets/video/youtube2.mp4" class="img-fluid rounded z-depth-1" controls=true autoplay=true %}
  </div> 
</div>
<div class="row"> 
  <div class="col-sm mt-3 mt-md-0"> 
        {% include video.liquid path="assets/video/youtube6.mp4" class="img-fluid rounded z-depth-1" controls=true autoplay=true %}
  </div> 
</div>

- **Advanced Object Recognition**: We employed special techniques to recognize equipment from a distance, despite their relatively small size in video frames, by developing custom algorithms for small object detection.
- **Challenging Environment Adaptability**: Our solution is engineered to withstand harsh construction conditions, such as dust, smoke, fog, and various lighting challenges, including low light and glare, ensuring reliable performance under all conditions.
- **Complex Activity Recognition**: Advanced algorithms differentiate between fine-grained heavy equipment operations, such as an excavator performing excavation vs moving to/from the worksite, and dump truck operations like loading, unloading, and idling.
- **Integration and Scalability**: Designed for seamless compatibility with existing camera infrastructure on construction sites, our solution eliminates the need for additional hardware installations and is easily scalable across multiple projects.
- **AI-Driven Enhancements**: We leveraged synthetic data and data augmentation techniques, including Generative Adversarial Learning, to simulate construction environments and enhance system accuracy and reliability.


## Model Development and Testing

### Data Collection

Limited video data was provided by the client for training, which we supplemented with data extracted from various public sources. Our team curated and extracted web video data, facing the challenge that publicly available construction datasets were often very noisy. Many videos, shot using cell phones at close range, were shaky, necessitating extensive cleanup, careful filtering, and annotation.

### Data Annotation

We recruited an in-house team of annotators for this project. Developing clear guidelines for the team proved challenging, necessitating an iterative process that included an evaluation phase. During this phase, we continuously refined the guidelines. Annotators were only approved for production annotation after achieving satisfactory accuracy levels in the evaluation phase.

Annotation requirements were extensive. The work encompassed various models, including equipment detection, classification, and activity recognition. The diversity of data was also critical. Data was categorized based on various sources to ensure diversity at every level. For instance, stock videos are generally cleaner, whereas YouTube videos are noisier. Longer videos were not overrepresented to avoid repetitive occurrences of similar images within the dataset.

Various annotation tools were used, such as CVAT and Labelbox.

### Active Learning

Active learning strategies were employed to minimize annotation requirements. Models would automatically annotate samples, and only corrections made by annotators were required. This greatly improved annotation speed.

### Image Augmentation

To address the need to handle various technical challenges, including clutter, occlusion, diverse lighting & camera angles, and diversity of equipment, extensive data augmentation was performed. Additionally, synthetic data was generated using Generative Adversarial Networks (GANs), contributing to the robustness of the model.

### Model Development

Various algorithms, models, and frameworks were tested, including a modified Faster R-CNN approach for object detection. The original model was not well-suited for recognizing small objects, so it was tailored to this specific use case.

### Activity Recognition

Various algorithms for deep activity recognition were tested to accurately identify and classify different construction site activities.

### Tracking

Kalman filtering was employed to track individual equipment through the site. Re-identification was a challenge that was overcome using Kalman filtering and visual similarity using DNN features.

## Business Impact

The deployment of our AI monitoring solution at client construction sites significantly improved operational efficiency and resource allocation. By offering real-time visibility into dump truck activities, our technology facilitated more effective scheduling, reduced idle times, and enabled better resource management, resulting in notable cost savings and enhanced productivity.

### Project Achievements

- **Enhanced Efficiency:** Improved scheduling and utilization of dump trucks, significantly reducing operational costs and enhancing project timelines.
- **Data-Driven Decision Making:** Provided invaluable insights into dump truck operations, empowering the client with information to influence future project management strategies.
- **Scalable and Versatile Solution:** Demonstrated the adaptability and scalability of our AI technology, highlighting its potential for broader applications within the construction industry and beyond.
- **Metrics for Productivity:** Enabled the measurement of equipment/labor activity and correlated with progress metrics from other sources such as drone data, facilitating smart estimation and bidding.

This report encapsulates our achievements in this client project, demonstrating technological innovation to solve the problem of digitizing and monitoring construction site operations. 