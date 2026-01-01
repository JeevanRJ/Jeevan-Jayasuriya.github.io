---
title: "Research on Firefighter Assistive Devices"
collection: research
---

Despite modern protective equipment, thousands of fireground injuries occur annually, underscoring the need for effective firefighter assistive technologies.
<img src="{{ site.baseurl }}/images/Slide9.PNG"
     alt="Research figure"
     style="width: 300px; max-width: 100%; display: block; margin: 1.5em auto;">

### Can a firefighter exoskeleton help?

The lack of firefighter-specific biomechanical data remains a major challenge in the design of effective assistive devices and exoskeletons. To address this gap, we collected biomechanical data from professional firefighters to create a comprehensive database of firefighter movement and loading patterns. Firefighter activities were visualized using MVN software, and musculoskeletal simulations were performed in the AnyBody Modeling System by applying virtual forces corresponding to external loads. 
<img src="{{ site.baseurl }}/images/Slide10.PNG"
     alt="Research figure"
     style="width: 700px; max-width: 100%; display: block; margin: 1.5em auto;">
     
<img src="{{ site.baseurl }}/images/Slide11.PNG"
     alt="Research figure"
     style="width: 700px; max-width: 100%; display: block; margin: 1.5em auto;">
     
<div style="max-width: 700px; margin: 2em auto;">
  <iframe
    src="https://www.youtube.com/embed/h34h2JHa8yo?si=xljKIuW746fjBHvA"
    style="width: 100%; aspect-ratio: 16 / 9;"
    frameborder="0"
    allowfullscreen>
  </iframe>
</div>

<div style="max-width: 700px; margin: 2em auto;">
  <iframe
    src="https://www.youtube.com/embed/RsNdsJtFUjg"
    style="width: 100%; aspect-ratio: 16 / 9;"
    frameborder="0"
    allowfullscreen>
  </iframe>
</div>
 
<div style="max-width: 700px; margin: 2em auto;">
  <iframe
    src="https://www.youtube.com/embed/ZiYy5dCg6oY?si=kmM51EpjpZJvvGvS"
    style="width: 100%; aspect-ratio: 16 / 9;"
    frameborder="0"
    allowfullscreen>
  </iframe>
</div>

### Closed-Loop Human–Machine Interfaces

Closed-loop human–machine interfaces are critical for the development of exoskeletons that prioritize safety, comfort, and performance. Shown below is an example using a simple PID controller implemented in the AnyBody Modeling System (AMS) to regulate the activation level of a targeted muscle during elbow flexion under an external load (black arrow). 
<img src="{{ site.baseurl }}/images/Slide15.PNG"
     alt="Research figure"
     style="width: 700px; max-width: 100%; display: block; margin: 1.5em auto;">
     
Developing control systems that explicitly account for human–exoskeleton interactions can reduce the number of iterations required during prototyping. 
 
<div style="max-width: 700px; margin: 2em auto;">
  <iframe
    src="https://www.youtube.com/embed/sOe8CmO5w4Y?si=IG2v_kkaX_ABsvgx"
    style="width: 100%; aspect-ratio: 16 / 9;"
    frameborder="0"
    allowfullscreen>
  </iframe>
</div>

### Hardware and Control Architecture

Actuators were selected to match the biomechanical demands of firefighter activities (joint range of motion and torque requirements) while minimizing system weight, size, and cost. Controller–actuator communication was established using CAN bus. Multiple active and passive control strategies were evaluated, with an emphasis on safety and smooth, reliable performance.

<img src="{{ site.baseurl }}/images/Slide17.PNG"
     alt="Research figure"
     style="width: 700px; max-width: 100%; display: block; margin: 1.5em auto;">

<img src="{{ site.baseurl }}/images/Slide18.png"
     alt="Zero Interaction Force Controller"
     style="width: 700px; max-width: 100%; display: block; margin: 2em auto;">

     
<!-- <img src="{{ site.baseurl }}/images/Slide18.PNG"
     alt="Research figure"
     style="width: 100px; max-width: 100%; display: block; margin: 1.5em auto;"> -->
     
<img src="{{ site.baseurl }}/images/Slide19.PNG"
     alt="Research figure"
     style="width: 700px; max-width: 100%; display: block; margin: 1.5em auto;">
Multiple design concepts were developed in SolidWorks and iteratively refined based on feedback from professional firefighters. 
<img src="{{ site.baseurl }}/images/Slide20.PNG"
     alt="Research figure"
     style="width: 600px; max-width: 100%; display: block; margin: 1.5em auto;">
