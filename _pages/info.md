---
layout: page
toc: false
title: Participant Info
short_title: Info
sidebar: true
icon: fa fa-calendar
order: 2
---

## Registration

* Registration (TBD - The contest is open to both industry and academia.)


## Target Platform 

The 2023 contest will use the [Kria KV260 Vision AI Starter Kit](https://www.xilinx.com/products/som/kria/kv260-vision-starter-kit.html) and the [Jetson Nano Developer Kit](https://developer.nvidia.com/embedded/jetson-nano-developer-kit).

### GPU Platform

The base design framework is provided here: <https://github.com/dac-sdc/gpu_starter_2023>.  **This repository is a work in progress and should be available by late March**

### FPGA Platform

You should use the Ubuntu 22.04 PYNQ PYNQ image, available at <http://www.pynq.io/board.html>.

The base design framework, with additional setup instructions, is provided here: <https://github.com/dac-sdc/fpga_starter_2023>. 

## Training Dataset

Link to download training dataset: <https://drive.google.com/file/d/1ceQ5y_rCReSZ26HzzCf2muDNbovjyl5k/view?usp=share_link>

The training dataset contains:
 * 10000 training images in the *JPEGImages* directory:
    * Some extra images with *_1* suffix are included such as 00009_1.jpg, which are simply mirror images of the base image and can be ignored.
    * The images have varied size, with the following distribution of sizes:
      * 1920x1080: 4962 images
      * 1280x720: 4552 images
      * 1920x1088: 404 images
      * 1920x1072: 82 images


 * Labelled object types and locations in the *label* directory.  For example, *JPEGImages/00001.jpg* will have an associated *label/00001.json* file describe object types and locations in the image.
 * Object types:

| Type | Name | Example | Identifying Data |
|------|------|---------|------------------|
|1|Motor Vehicle | <img src="{% link media/dataset/motor_vehicle.png %}"> | Bounding Box |
|2|Non-motorized Vehicle|<img src="{% link media/dataset/nonmotor_vehicle.png %}"> | Bounding Box |
|3|Pedestrian|<img src="{% link media/dataset/pedestrian.png %}"> | Bounding Box |
|4|Red Traffic Light|<img src="{% link media/dataset/red_light.png %}"> | Bounding Box |
|5|Yellow Traffic Light|<img src="{% link media/dataset/yellow_light.png %}"> | Bounding Box |
|6|Green Traffic Light|<img src="{% link media/dataset/green_light.png %}"> | Bounding Box |
|7|Off Traffic Light|<img src="{% link media/dataset/off_light.png %}"> | Bounding Box |

## Test Dataset
The hidden test dataset contains 6000 images.  The images have varied size, with the following distribution of sizes:
  * 1920x1080: 3788 images
  * 1280x720: 1932 images
  * 1920x1088: 243 images
  * 1920x1072: 37 images
*Note we will only use 3000 images for the preliminary submissions and use all 6000 images for the final evaluation. All the designs will be evaluated based on Batch Size = 1.*

## Other Info

### Frequently Asked Questions
  * [FAQs]({% link _pages/faq.md %})

### Previous Contest Winning Designs
*Note:* These are designs for the GPU and FPGA contest, and were for a different image detection problem/dataset than this year.

  * 2023: <https://github.com/PKU-SEC-Lab/dac-sdc-2023-designs>
  * 2022: <https://github.com/jgoeders/dac_sdc_2022_designs>
  * 2021: <https://github.com/jgoeders/dac_sdc_2021_designs>
  * 2020: <https://github.com/jgoeders/dac_sdc_2020_designs>
  * 2019: <https://github.com/xyzxinyizhang/2019-DAC-System-Design-Contest>
  * 2018: <https://github.com/xyzxinyizhang/2018-DAC-System-Design-Contest>


## Q&A Platform
See Slack link on sidebar.

