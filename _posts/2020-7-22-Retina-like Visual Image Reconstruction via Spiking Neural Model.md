---
layout: post
title: Retina-like Visual Image Reconstruction via Spiking Neural Model
categories:
- blog
---

The high-sensitivity vision of primates, including humans, is mediated by a small retinal region called the fovea. As a novel bio-inspired vision sensor, spike camera mimics the
fovea to record the nature scenes by continuous-time spikes instead of frame-based manner. However, reconstructing visual images from the spikes remains to be a challenge. In this paper, we design a retina-like visual image reconstruction framework, which is flexible in reconstructing full texture of natural scenes from the totally new spike data.
Specifically, the proposed architecture consists of motion local excitation layer, spike refining layer and visual reconstruction layer motivated by bio-realistic leaky integrate
and fire (LIF) neurons and synapse connection with spiketiming-dependent plasticity (STDP) rules. This approach may represent a major shift from conventional frame-based vision to the continuous-time retina-like vision, owning to the advantages of high temporal resolution and low power consumption. To test the performance, a spike dataset is constructed which is recorded by the spike camera. The experimental results show that the proposed approach is extremely effective in reconstructing the visual image in both normal and high speed scenes, while achieving high dynamic
range and high image quality.

---


### The framework
![](https://github.com/Crazyspike/crazyspike.github.io/img/cvpr-2783.jpg)
![](http://i.imgur.com/Pmzk4j1.png)
![](http://i.imgur.com/Pmzk4j1.png)


### The results


