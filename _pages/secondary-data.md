---
title: "Secondary Data"
permalink: /secondary-data/
layout: archive
author_profile: true
last_modified_at: 2026-05-23
show_disclaimer: true
---

{% include base_path %}

# What is secondary data?

<div style="display: flex; gap: 20px;">
  <div style="flex: 1;">
    <strong>Secondary data</strong> is contextual ecological information incidentally captured in an image, such as habitats, species interactions, physiological state, phenology, morphology, ontogeny, and sex (<a href="https://doi.org/10.1093/biosci/biaa131">Callaghan et al., 2021</a>; <a href="https://doi.org/10.1002/2688-8319.12295">Pernat et al., 2024</a>). Secondary data is described on iNaturalist as "<a href="https://help.inaturalist.org/en/support/solutions/articles/151000191830-what-are-the-definitions-of-inaturalist-annotations-">annotations</a>" and can be manually added to observations.<br>
  </div>
  <div style="flex: 1;">
    <img src="..\images\secondary_data_definition_fig.png" alt="Secondary data definition figure">
  </div>
</div>

### Why study secondary data?

Digital images are untapped sources of ecological discovery. Through secondary data, we can study any physical, observational event to better understand a species' ecology and biology. This information has already been used, for example, to support taxonomic classifications ([Mesaglio et al., 2025](https://doi.org/10.1002/ajb2.70048)), indicate changing climate conditions ([Steinke et al., 2025](https://doi.org/10.1111/gcb.70365)), and reveal new species interactions ([Zamani et al., 2024](https://doi.org/10.1080/00222933.2024.2382404)), and host associations ([Zhang et al., 2022](https://doi.org/10.11646/zootaxa.5168.1.5)). In addition to these direct uses of secondary data for ecological discovery, there remains much unexplored potential for indirect applications of secondary data, which I aim to demonstrate through [my Master's thesis work](../_pages/projects.md#masters-thesis-research-on-secondary-image-data). Moreover, secondary data is applicable to all digital images, including pictures uploaded to participatory scientist platforms, digitized museum records, and images collected from insect and wildlife camera traps (e.g., [Steinke et al., 2025](https://doi.org/10.1111/gcb.70365)).

### Who can use secondary data?

Secondary data provides exciting opportunities for **both participatory scientists and academics**. Because secondary data must be *manually* extracted from images (see below for info on automated data extraction), ecological discovery from secondary data can be somewhat situational or coincidental in the traditional sense of "discovery," such as finding an image of a species exhibiting a new behavior or interaction. On the other hand, discoveries can be intentional in cases where images are being intentionally searched for secondary data and then statistical analyses performed on the data reveal some "discovery." Both examples indicate that ecological discovery from secondary data can be made by anyone!


### How do we get secondary data?

Currently, extracting secondary data from images is a manual effort, where you must look at the image and determine whether it contains the secondary data of interest. Much of the current research on secondary data has relied on manual data extraction because secondary data can take many forms (e.g., habitat, morphology, behavior). On iNaturalist, it is possible to add "annotations" to images observations, but many observations lack annotations. Additionally, because secondary data comes in many forms, it would be quite difficult to annotate every observation with all the secondary data it contains.

Through recent advancements in computer vision, researchers are applying deep learning models to automate the extraction of secondary data. I want to emphasize that "automate" does not necessarily replace humans in the process of retrieving secondary data from images. *Streamline* would be a better term to describe how AI models are facilitating the process of secondary data extraction because humans are still heavily involved in how the data is retrieved and analyzed.

A classic approach involves fine-tuning general foundation image classification models. In [Alyetama et al. (2025)](https://www.biorxiv.org/content/10.1101/2025.09.30.678090v1), the authors fine-tuned a YOLOv8 image classification model to classify mammal tracks and signs. However, the approach applied in Alyetama et al. is restricted to the particular applications on which the model was trained; in this case, you can only use this model for distinguishing mammal tracks and signs, so you would need to create more models for other types of secondary data.

<div style="display: flex; gap: 20px;">
  <div style="flex: 1;">
    Much more recently, the rise of multimodal models possess exceptional capabilities beyond the traditional unimodal model (think of "modal" as a data type, like image, text, or audio). Image classification models are a classic unimodal model that is trained only on images, whereas multimodal models can be trained on multiple modalities, such as both image and text. Research by the <a href="https://imageomics.osu.edu/">Imageomics Institute</a> has focused on creating foundation multimodal models for the <i>biological</i> domain to take advantage of multimodality and reduce the need for fine-tuning general foundation models. For example, <a href="https://arxiv.org/abs/2505.23883">Gu et al. (2025)</a> developed BioCLIP 2, a biological-based vision-language foundation model that is effective for species classification. The INQUIRE benchmark (<a href="https://doi.org/10.52202/079017-4018">Vendrow, Pantazis et al., 2024</a>) and the INQUIRE-Search framework (<a href="https://doi.org/10.48550/arXiv.2511.15656">Vendrow, Chae, Kurinchi-Vendhan et al., 2025</a>) offer the first attempts for automating secondary data extraction using foundation multimodal models. In <a href="https://doi.org/10.52202/079017-4018">Vendrow, Pantazis et al. (2024)</a>, the authors created a "benchmark" of search queries and evaluated the performance on general foundation models for retrieving secondary data. This benchmark can be used to evaluate the performance of new models for this secondary data retrieval task. In <a href="https://doi.org/10.48550/arXiv.2511.15656">Vendrow, Chae, Kurinchi-Vendhan et al. (2025)</a>, the authors use the highest performing general foundation model from the other paper and demonstrate how these models can streamline ecological discovery with secondary data through a series of case studies.
  </div>
  <div style="flex: 1;">
    <img src="..\images\inquire-search-vendrow-et-al-2025.png" alt="Figure 2 from Vendrow, Chae, Kurinchi-Vendhan et al., 2025"><br>
    Figure 2 from <a href="https://doi.org/10.48550/arXiv.2511.15656">Vendrow, Chae, Kurinchi-Vendhan et al., 2025</a> demonstrating the INQUIRE-Search framework (reproduced under CC BY-NC-SA 4.0).<br>
  </div>
</div>

So, we have the existing technology that is capable of automating, or streamlining, the extraction of secondary data. And we also have a framework for the secondary data retrieval process. However, there is a lack of readily-available tools for anyone to use. [Vendrow, Chae, Kurinchi-Vendhan et al. (2025)](https://doi.org/10.48550/arXiv.2511.15656) *do* have a [web-hosted version of INQUIRE-Search](http://inquire-demo.csail.mit.edu/); unfortunately, this interface has never worked on my computers (perhaps it will for yours?). I have preliminary explored ways to develop an accessible interface for streamlining the exploration of secondary data (see below for more information about the [Secondary Data Explorer](#the-secondary-data-explorer)). I am interested in improving accessibility of tools related to secondary data for researchers and participatory scientists alike.


# Table of Contents

See below the topics below for more information, explanation, resources, and tools related to secondary data!

* My work on secondary data
  * [My Master's thesis research](#my-masters-thesis-reserach)
  * [The "Secondary Data Explorer"](#the-secondary-data-explorer)
* Others' work on secondary data
  * Secondary data in wildlife & insect camera trap images
  * Automated extraction of secondary data
* Related topics
  * [Vibe coding](#vibe-coding)


## My Master's thesis reserach

TBD

## The Secondary Data Explorer

The [**Secondary Data Explorer**](https://ktorres23.github.io/ecology-vibe-coding/pages/secondary_explorer.html) emerged from an interest to:

1. automate secondary data extraction,
2. showcase how awesome [**vibe coding**](#vibe-coding) is, and
3. provide accessible tools for both researchers and participatory scientists.

...TBD

## Vibe Coding

TBD