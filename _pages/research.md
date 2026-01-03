---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

{% include base_path %}

## Contents

- [Research Overview](#research-overview)
- [Research on Spaceflight Human Optimization](#research-on-spaceflight-human-optimization)
- [Research on Firefighter Assistive Devices](#research-on-firefighter-assistive-devices)   
- [Fire safety in coal yards](#fire-safety-in-coal-yards)
- [Other undergraduate research](#other-undergraduate-research)
- [Industrial internship projects](#industrial-internship-projects)


## Research Overview {#research-overview}

<div style="max-width: 820px; font-size: 1.05em; line-height: 1.7; margin-bottom: 3em;">

My research focuses on analyzing <strong>multimodal physiological and behavioral data</strong> to understand how human sensorimotor control and performance vary under challenging conditions such as <strong>space travel</strong> and <strong>firefighting</strong>, as well as during <strong>human–machine interactions</strong> where system design and autonomy influence human behavior.</br>


To achieve this, I integrate insights from <strong>brain imaging</strong>, <strong>movement kinematics</strong>, <strong>eye gaze</strong>, <strong>muscle activation</strong>, <strong>heart rate</strong>, and <strong>subjective perception</strong>, together with <strong>musculoskeletal analysis</strong> and <strong>data-driven methods</strong> including <strong>statistics, machine learning, and deep learning–based temporal models</strong>, to capture <strong>neural, biomechanical, and perceptual markers</strong> of human state.


The overarching goal of my research is to translate these data-driven insights into the <strong>design and control of human–machine systems</strong> that jointly optimize <strong>human performance, system effectiveness, and safety</strong>.


Following is a short description of my research work. Selected analysis code and tools are available on my [GitHub repository](https://github.com/JeevanRJ?tab=repositories).

</div>

<hr style="margin: 2.5em 0;">

{% for post in site.research reversed %}
  {% include archive-single-research.html %}
{% endfor %}
