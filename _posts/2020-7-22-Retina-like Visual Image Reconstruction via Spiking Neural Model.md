---
layout: post
title: Retina-like Visual Image Reconstruction via Spiking Neural Model
categories:
- blog
---

The high-sensitivity vision of primates, including humans, is mediated by a small retinal region called the fovea. As a novel bio-inspired vision sensor, spike camera mimics the
fovea to record the nature scenes by continuous-time spikes instead of frame-based manner. However, reconstructing visual images from the spikes remains to be a challenge. In this paper, we design a retina-like visual image reconstruction framework, which is flexible in reconstructing full texture of natural scenes from the totally new spike data. Specifically, the proposed architecture consists of motion local excitation layer, spike refining layer and visual reconstruction layer motivated by bio-realistic leaky integrate and fire (LIF) neurons and synapse connection with spiketiming-dependent plasticity (STDP) rules. This approach may represent a major shift from conventional frame-based vision to the continuous-time retina-like vision, owning to the advantages of high temporal resolution and low power consumption. To test the performance, a spike dataset is constructed which is recorded by the spike camera. The experimental results show that the proposed approach is extremely effective in reconstructing the visual image in both normal and high speed scenes, while achieving high dynamic range and high image quality.

---


## The framework

<div align=center><img src="https://raw.githubusercontent.com/Crazyspike/crazyspike.github.io/master/img/CVPR-2783.jpg" width="500" alt="fig1"/></div>

<p align="left">The spike camera based on fovea-like sampling and visual image reconstruction. In FSM, the intensity of light is converted into voltage by the photoreceptor. Once the voltage reaches a predefined threshold, a one-bit spike is output and a signal to reset the integrator is dispatched at the same time. This process is quite similar to the integrate-and-fire neuron. Different luminance stimuli I leads to a different spike firing rate, the output and the reset are triggered asynchronously among various pixels.</p>

<div align=center><img src="https://raw.githubusercontent.com/Crazyspike/crazyspike.github.io/master/img/CVPR-27831.jpg" width="500" alt="fig2"/></div>

<div align=center><img src="https://raw.githubusercontent.com/Crazyspike/crazyspike.github.io/master/img/CVPR-27832.jpg" width="500" alt="fig3"/></div>

<p align="left">The overall architecture and the microscopic analysis of spiking neural model. (a) The input spike data is converted to spike plane (black dashed box) and spike train (red dashed box). The spike plane connects to the motion local excitation layer, and the dynamic neurons at this moment are marked, while the spike train with the mark information input to the next layer. (b) The noise spikes are eliminated by the mechanism of the refractory period while the static and dynamic spikes are preserved. (c) Each input spikes yield a potential according to STDP, and if the accumulated membrane potential reaches the threshold, the model is adaptively adjusted to fit the input spikes.</p>
---
## The results

<div align=center><img src="https://raw.githubusercontent.com/Crazyspike/crazyspike.github.io/master/img/CVPR-27833.jpg" width="500" alt="fig4"/></div>

<p align="left">The reconstruction results on Class A and B. We compared our method with TFW, TFI and TFA on Class A. Since TFP and TFA have no ability to reconstruct dynamic scenes, we only compare our methods with TFI on Class B.</p>

<div align=center><img src="https://raw.githubusercontent.com/Crazyspike/crazyspike.github.io/master/img/CVPR-27835.jpg" width="500" alt="fig5"/></div>
  
<p align="left">The reconstruction results of different vision sensors.</p>

---

###[Dataset](https://www.pkuml.org/resources/pku-spike-recon-dataset.html)
###[Poster](https://raw.githubusercontent.com/Crazyspike/crazyspike.github.io/master/img/poster-2783.pdf)
###[Oral slide](https://www.slideshare.net/secret/mZdvclfFoD4IVh)
###[PDF](https://openaccess.thecvf.com/content_CVPR_2020/papers/Zhu_Retina-Like_Visual_Image_Reconstruction_via_Spiking_Neural_Model_CVPR_2020_paper.pdf)
