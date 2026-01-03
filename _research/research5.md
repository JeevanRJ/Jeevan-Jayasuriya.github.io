---
title: "Research on spaceflight human optimization"
collection: research
---

### Multiple Spaceflight Hazards {#multiple-spaceflight-hazards}

Sensorimotor function has been critical to mission success in past space missions and will be even more essential for future long-duration missions to Mars and beyond, where real-time ground support will be limited. During spaceflight, astronauts are exposed to multiple hazards, including altered gravity and fatigue arising from high workload and sleep deprivation.

Do these stressors jointly impair sensorimotor function, or can humans adapt to sustain performance under such challenging conditions?

To address this question, we conducted human-subject experiments while collecting multimodal physiological data, including brain imaging, eye tracking, full-body kinematics, muscle activity, and heart rate. This approach enables us to identify both performance impairments and compensatory mechanisms underlying human adaptation.
<!-- ![Research figure]({{ site.baseurl }}/images/Slide1.PNG) -->
<img src="{{ site.baseurl }}/images/Slide1.PNG"
     alt="Research figure"
     style="width: 400px; max-width: 100%; display: block; margin: 1.5em auto;">

### Data Collection and Synchronization {#data-collection-and-synchronization}

Multimodal data streams were synchronized using Lab Streaming Layer (LSL). Devices were wirelessly networked to dedicated acquisition systems, with automated error-checking implemented to support robust, high-fidelity data collection. 
<img src="{{ site.baseurl }}/images/Slide2.PNG"
     alt="Research figure"
     style="width: 700px; max-width: 100%; display: block; margin: 1.5em auto;">

### Simulating Altered Gravity {#simulating-altered-gravity}

Post-landing effects associated with altered gravity were recreated in the laboratory using Galvanic Vestibular Stimulation (GVS). A small, controlled electrical current (up to 2 mA) was applied across the mastoid processes, generating an electric field that perturbs vestibular afferent signaling. This stimulation effectively disrupts vestibular input to the brain, allowing controlled investigation of balance and sensorimotor responses under altered gravity–like conditions. 
<img src="{{ site.baseurl }}/images/Slide3.PNG"
     alt="Research figure"
     style="width: 600px; max-width: 100%; display: block; margin: 1.5em auto;">
### Sensorimotor test battery {#sensorimotor-test-battery}

Participants completed a sensorimotor test battery consisting of 13 activities under the combined effects of GVS and fatigue.
<img src="{{ site.baseurl }}/images/Slide4.PNG"
     alt="Research figure"
     style="width: 500px; max-width: 100%; display: block; margin: 1.5em auto;">

### Fatigue Manipulation and Assessment {#fatigue-manipulation-and-assessment}

Mental fatigue, representing work overload, was induced using a two-back task that required continuous engagement in a working memory task for two hours. Sleep-deprivation–related fatigue was induced by requiring participants to remain awake overnight while repeating the sensorimotor test battery at four equally spaced time points throughout the night. 
In addition to multimodal physiological measurements, fatigue was assessed using the Psychomotor Vigilance Test (PVT), Karolinska Sleepiness Scale (KSS), and Profile of Mood States (POMS).
<img src="{{ site.baseurl }}/images/Slide5.PNG"
     alt="Research figure"
     style="width: 600px; max-width: 100%; display: block; margin: 1.5em auto;">

### Key Findings and Ongoing Work {#key-findings-and-ongoing-work}

Our analyses revealed distinct physiological responses in brain activation and other physiological measures under the interactive effects of altered gravity and fatigue. Related journal publications are currently in preparation. 
<img src="{{ site.baseurl }}/images/Slide6.PNG"
     alt="Research figure"
     style="width: 500px; max-width: 100%; display: block; margin: 1.5em auto;">

### Assistive Technologies for Planetary Surface Exploration {#assistive-technologies-for-planetary-surface-exploration}

Post-landing sensorimotor impairment remains a major operational risk for astronauts during planetary surface exploration, particularly when immediate external mobility support may be limited. Can gait instabilities be predicted in advance, enabling assistive systems to provide early warnings and allowing exoskeletons to transition smoothly into fall-prevention modes?  
<img src="{{ site.baseurl }}/images/Slide7.PNG"
     alt="Research figure"
     style="width: 500px; max-width: 100%; display: block; margin: 1.5em auto;">

In this work, we trained a Temporal Convolutional Network (TCN) to forecast gait instability 0.1–1.0 s into the future using margin of stability, muscle activation, and kinematic data. 

<!-- <div style="max-width: 1100px; margin: 2em auto;">
  <iframe
    src="https://www.youtube.com/embed/3paX5J4QHCg?si=LtNg_zyurS0PHtFm"
    style="width: 100%; aspect-ratio: 16 / 9;"
    frameborder="0"
    allowfullscreen>
  </iframe>
</div> --> 

<div style="max-width: 700px; margin: 2em auto;">
  <iframe
    src="https://www.youtube.com/embed/3paX5J4QHCg"
    style="width: 100%; aspect-ratio: 16 / 9;"
    frameborder="0"
    allowfullscreen>
  </iframe>
</div>

