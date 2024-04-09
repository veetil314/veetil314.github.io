---
layout: page
title: Heavy Equipment Monitoring with AI for Top 5 Construction Firm in Asia Pacific 
description: Reflective AI technology to measure heavy equipment activity in civil construction projects from HD video feeds for client.
img: assets/img/3.jpg
importance: 2
category: work
giscus_comments: false
---

<h2>Project Overview</h2>
<p>In a significant leap towards enhancing efficiency in civil construction projects, our team at Reflective AI embarked on a mission to revolutionize how heavy equipment, specifically dump trucks, is monitored and managed. Collaborating with one of the largest construction firms in the Asia Pacific region, we aimed to leverage advanced AI-driven video recognition technology. This technology provides real-time, actionable insights into heavy equipment and manpower, beginning with dump truck operations, thereby addressing critical operational bottlenecks and enhancing overall project efficiency.
</p>

<h2>Problem</h2>
<p>
The initial digitization focus was on earthwork operations, with plans to expand to other areas, including building construction and manual operations. Earthwork is a substantial cost factor in large infrastructure projects, involving numerous trucks transporting materials, excavators performing cut and fill operations and more. Understanding and digitizing these operations was essential but challenging with traditional technologies including IoT sensors, due to the high turnover of independent equipment operators leading to challenges in deep IoT integration. A camera-based solution emerged as an effective method to bypass these challenges, helping to eliminate bottlenecks, delays, and simplify integration.
</p>

<h2>Solution</h2>
<p>
We developed technology to intelligently recognize the fine-grained activity of heavy equipment, such as whether it's loaded/unloaded, counting the number of dumps, and distinguishing between moving and idle states. This approach offers a detailed overview of material movement, utilization, and productivity without requiring complex infrastructure. A few cameras covering the work area, necessary for security and monitoring, are used.

An easy-to-use UI generates a smart video summary that highlights key activities like dump truck activity.  Heatmaps are created to show areas of high activity over a day or fixed period of time , and metrics reveal the percentage of idle time, detailed equipment activity and the spatial distribution of activity.
</p>


- **Title 1  
with a line break**: Description 1  
also with a line break
- **Title 2**: Description 2  
with a line break
- **Title 3  
with multiple  
line breaks**: Description 3

<h2>Key Technology Highlights</h2>
    
        - **Advanced Object Recognition**: 
        We employed special techniques to recognize equipment from a distance, despite their relatively small size in video frames, by developing custom algorithms for small object detection.

        - **Challenging Environment Adaptability**: 
        Our solution is engineered to withstand harsh construction conditions, such as dust, smoke, fog, and various lighting challenges, including low light and glare, ensuring reliable performance under all conditions.

        - **Complex Activity Recognition**: 
        Advanced algorithms differentiate between fine-grained heavy equipment operations, such as an excavator performing excavation vs moving to/from the worksite, and dump truck operations like loading, unloading, and idling.

        - **Integration and Scalability**: 
        Designed for seamless compatibility with existing camera infrastructure on construction sites, our solution eliminates the need for additional hardware installations and is easily scalable across multiple projects.

        - **AI-Driven Enhancements**: 
        We leveraged synthetic data and data augmentation techniques, including Generative Adversarial Learning and curriculum learning, to simulate construction environments and enhance system accuracy and reliability.


  <h2>Model Development and Testing</h2>
    <h3>Data Collection</h3>
    <p>Limited video data was provided by the client for training, which we supplemented with data extracted from various public sources. Our team curated and extracted web video data, facing the challenge that publicly available construction datasets were often very noisy. Many videos, shot using cell phones at close range, were shaky, necessitating extensive cleanup, careful filtering, and annotation.</p>
    <h3>Data Annotation</h3>
    <p>We recruited an in-house team of annotators for this project. Developing clear guidelines for the team proved challenging, necessitating an iterative process that included an evaluation phase. During this phase, we continuously refined the guidelines. Annotators were only approved for production annotation after achieving satisfactory accuracy levels in the evaluation phase.</p>
    <p>Annotation requirements were extensive. The work encompassed various models, including equipment detection, classification, and activity recognition. The diversity of data was also critical. Data was categorized based on various sources to ensure diversity at every level. For instance, stock videos are generally cleaner, whereas YouTube videos are noisier. Longer videos were not overrepresented to avoid repetitive occurrences of similar images within the dataset.</p>
    <p>Various annotation tools were used, such as CVAT and Labelbox.</p>
    <h3>Active Learning</h3>
    <p>Active learning strategies were employed to minimize annotation requirements. Models would automatically annotate samples, and only corrections made by annotators were required. This greatly improved annotation speed.</p>
    <h3>Image Augmentation</h3>
    <p>To address the need to handle various technical challenges, including clutter, occlusion, diverse lighting & camera angles, and diversity of equipment, extensive data augmentation was performed. Additionally, synthetic data was generated using Generative Adversarial Networks (GANs), contributing to the robustness of the model.</p>
    <h3>Model Development</h3>
    <p>Various algorithms, models, and frameworks were tested, including a modified Faster R-CNN approach for object detection. The original model was not well-suited for recognizing small objects, so it was tailored to this specific use case.</p>
    <h3>Activity Recognition</h3>
    <p>Various algorithms for deep activity recognition were tested to accurately identify and classify different construction site activities.</p>
    <h3>Tracking</h3>
    <p>Kalman filtering was employed to track individual equipment through the site. Re-identification was a challenge that was overcome using Kalman filtering and visual similarity using DNN features.</p>
    <h2>Business Impact</h2>
    <p>The deployment of our AI monitoring solution at client construction sites significantly improved operational efficiency and resource allocation. By offering real-time visibility into dump truck activities, our technology facilitated more effective scheduling, reduced idle times, and enabled better resource management, resulting in notable cost savings and enhanced productivity.</p>
    <h3>Project Achievements</h3>
    <ul>
        <li><strong>Enhanced Efficiency:</strong> Improved scheduling and utilization of dump trucks, significantly reducing operational costs and enhancing project timelines.</li>
        <li><strong>Data-Driven Decision Making:</strong> Provided invaluable insights into dump truck operations, empowering the client with information to influence future project management strategies.</li>
        <li><strong>Scalable and Versatile Solution:</strong> Demonstrated the adaptability and scalability of our AI technology, highlighting its potential for broader applications within the construction industry and beyond.</li>
        <li><strong>Metrics for Productivity:</strong> Enabled the measurement of equipment/labor activity and correlated with progress metrics from other sources such as drone data, facilitating smart estimation and bidding.</li>
    </ul>
    <p>This report encapsulates our achievements in this client project, demonstrating our commitment to technological innovation and its tangible benefits in real-world applications. It highlights our role in advancing construction site operations through AI, setting the stage for future projects poised to transform the industry.</p>



<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Caption photos easily. On the left, a road goes through a tunnel. Middle, leaves artistically fall in a hipster photoshoot. Right, in another hipster photoshoot, a lumberjack grasps a handful of pine needles.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This image can also have a caption. It's like magic.
</div>

You can also put regular text between your rows of images.
Say you wanted to write a little bit about your project before you posted the rest of the images.
You describe how you toiled, sweated, _bled_ for your project, and then... you reveal its glory in the next row of images.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    You can also have artistically styled 2/3 + 1/3 images, like these.
</div>

The code is simple.
Just wrap your images with `<div class="col-sm">` and place them inside `<div class="row">` (read more about the <a href="https://getbootstrap.com/docs/4.4/layout/grid/">Bootstrap Grid</a> system).
To make images responsive, add `img-fluid` class to each; for rounded corners and shadows use `rounded` and `z-depth-1` classes.
Here's the code for the last row of images above:

{% raw %}

```html
<div class="row justify-content-sm-center">
  <div class="col-sm-8 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm-4 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
```

{% endraw %}
