---
layout: archive
title: "Research Overview"
permalink: /research/
author_profile: true
---

My research focuses on analyzing multimodal physiological and behavioral data to understand how human sensorimotor control and performance vary under challenging conditions such as space travel and firefighting, as well as during human–machine interactions where system design and autonomy influence human behavior.

To achieve this, I integrate insights from brain imaging, movement kinematics, eye gaze, muscle activation, heart rate, and subjective perception, together with musculoskeletal analysis and data-driven methods including statistics, machine learning, and deep learning–based temporal models, to capture neural, biomechanical, and perceptual markers of human state.

The overarching goal of my research is to translate these data-driven insights into the design and control of human–machine systems that jointly optimize human performance, system effectiveness, and safety.

---

{% include base_path %}

{% for post in site.research reversed %}
  {% include archive-single.html %}
{% endfor %}





