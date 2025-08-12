---
title: "mbt Conference 3.0 Workshop: Real-time Neuroergonomics"
date: 2025-01-15
aliases: 
    - /workshops/neuroergonomics-live
    - /mbt-conference/workshop-3.0
tags: ["mobile EEG","neuroergonomics","multimodal recording","LSL","cognitive-motor interference","real-world neuroscience","MATLAB","EEGLAB","physiological measurements"]
author: ["Melanie Klapprott", "Emma Lieker", "Julian Elias Reiser"]
description: "A hands-on workshop introducing multimodal recording and analysis techniques for mobile brain/body imaging in real-world environments." 
summary: "This workshop provides practical experience with mobile EEG recording, multimodal data synchronization using Lab Streaming Layer (LSL), and analysis of cognitive-motor interference. Participants learn to record EEG, ECG, and eye-tracking data simultaneously, organize and merge multimodal datasets, and perform real-time analysis of neurophysiological responses during naturalistic tasks." 
cover:
    image: "neuroergonomics-live.png"
    alt: "Neuroergonomics Live Workshop"
    relative: true
editPost:
    URL: "https://github.com/julianreiser/usefulToolbox"
    Text: "Code Repository"
showToc: true
disableAnchoredHeadings: false
---

## Introduction

This workshop demonstrates how to go beyond traditional lab-based EEG and see how multimodal recordings come to life in real-world environments. Neuroergonomics combines modern neurotechnology with real-world work environments to objectively measure cognitive workload and human performance during naturalistic tasks.

The workshop addresses key questions in mobile brain/body imaging:

+ How do we synchronize multiple physiological data streams in real-time?
+ What challenges arise when recording outside controlled laboratory settings?
+ How can we analyze cognitive-motor interference using mobile EEG?
+ What are the practical considerations for multimodal data organization and analysis?

Modern work environments increasingly require humans to process information while moving, making mobile neuroimaging essential for understanding cognitive demands in ecological settings.

## Prerequisites and Software Requirements

This workshop requires specific software and hardware setup for multimodal data recording and analysis.

##### Core Requirements

+ **MATLAB** (R2008b or later) with the following toolboxes:
  - Signal Processing Toolbox
  - Statistics and Machine Learning Toolbox  
  - Optimization Toolbox
  - Image Processing Toolbox

##### Essential EEGLAB Setup

+ **EEGLAB** (2021.1 or newer) - [Download here](https://sccn.ucsd.edu/eeglab/download.php)
+ **Required EEGLAB Plugins:**
  - MoBILAB - for multimodal data import and synchronization
  - XDF Import Plugin - for Lab Streaming Layer file support
  - BIOSIG Toolbox - for various EEG formats (BDF, EDF)
  - bva-io Plugin (optional) - for BrainVision Analyzer compatibility

##### Additional Tools

+ **Lab Streaming Layer (LSL)** - for real-time data synchronization
+ **load_xdf function** - [MATLAB XDF loader](https://github.com/xdf-modules/xdf-Matlab/tree/master)
+ **Python environment** with lsl_relay_time_alignment package
+ **Visual Studio Code** for Python script execution

## Part 1: Understanding Neuroergonomics

This section introduces the theoretical foundation and practical motivation for mobile brain/body imaging.

##### Workshop Materials

+ [Workshop Slides](phttps://github.com/julianreiser/mbt-Conference-3.0-Workshop/blob/main/presentations/2025-04-13_mbtConference3.0_workshop.pdf) - Complete presentation covering theory and practice
+ [Data recorded during the workshop](https://nextcloud.mbraintrain.com/s/GgCqTpkHmxedjGs) - Why we need physiology in ergonomics

##### Key Concepts Covered

+ **Multiple Resource Theory** - Understanding cognitive-motor interference
+ **Mobile Brain/Body Imaging (MoBI)** - From lab to real-world measurements  
+ **Measurement Modalities:**
  - EEG (mBrainTrain Pro X) - neural activity measurement
  - ECG (Bittium Faros 180) - cardiac activity monitoring
  - Eye-tracking (Pupil Labs Neon) - gaze behavior analysis

##### Readings

+ [Dehais & Ayaz (2018)](https://doi.org/10.1016/B978-0-12-811926-6.00001-4) - Progress and direction in neuroergonomics


## Part 2: Data Recording and Synchronization

This section covers practical aspects of multimodal data recording using Lab Streaming Layer (LSL).

##### Live Demonstration

+ **Participant Preparation** - EEG cap setup, sensor placement, impedance checking
+ **LSL Setup** - Creating outlets, streaming multiple data sources
+ **Real-time Recording** - Using LabRecorder for synchronized data capture

##### Experimental Paradigms

+ **Finger Tapping Task** - Readiness potential (N100) measurement during voluntary movement
+ **Auditory Oddball** - P300 responses to natural stimuli (audience clapping)

## Part 3: Data Organization and Preprocessing

This section demonstrates proper data organization and merging of multimodal recordings.

##### Analysis Scripts

+ **[usefulLslAlign.m](code/usefulLslAlign.m)** - Import and merge multiple LSL streams and local files (.edf, .bdf, .xdf, .xlsx) into EEGLAB-compatible format
+ **[usefulMergePupilData.ipynb](code/usefulMergePupilData.ipynb)** - Merge Pupil Labs recordings with XDF files and cloud data
+ **[usefulQuickPrepro.m](code/usefulQuickPrepro.m)** - Quick preprocessing pipeline for workshop data

##### Data Organization Protocol

+ **File Structure Requirements** - Standardized folder organization for automated processing
+ **Multimodal Synchronization** - Time alignment across different recording systems  
+ **Quality Control** - Data validation and artifact identification

##### Practice Dataset

+ [Workshop Example Data](https://nextcloud.mbraintrain.com/s/GgCqTpkHmxedjGs) - Real recordings from the workshop for hands-on practice

## Part 4: Real-time Analysis and Visualization

This section covers rapid analysis techniques for mobile EEG data and real-time feedback applications.

##### Analysis Pipeline

+ **Preprocessing Steps:**
  - Artifact removal and filtering
  - Independent Component Analysis (ICA)
  - Channel interpolation and re-referencing

+ **Event-Related Potential Analysis:**
  - Readiness potential extraction
  - P300 component identification
  - Statistical analysis of ERP components

##### Visualization Tools

+ **Real-time Plotting** - Live EEG signal visualization during recording
+ **ERP Averaging** - Grand average computation and statistical testing
+ **Multimodal Integration** - Combining EEG, ECG, and eye-tracking metrics

## Advanced Topics and Applications

This section explores cutting-edge applications and research frontiers in mobile neuroergonomics.

##### Research Applications

+ **Cognitive-Motor Interference** - Dual-task paradigms in naturalistic settings
+ **Human-Machine Interaction** - Brain-computer interfaces for assistive technology
+ **Workplace Assessment** - Objective workload measurement in operational environments

##### Current Research Projects

+ [EEGManySteps Collaborative Study](https://eegmanysteps.org) - Multi-lab investigation of gait-related EEG

##### Future Directions

> The future of neuroergonomics lies in seamless integration of multiple physiological measures in naturalistic environments. As technology advances, we move toward continuous, unobtrusive monitoring that can provide real-time insights into human cognitive state and performance.

Mobile brain/body imaging represents a paradigm shift from controlled laboratory studies to ecologically valid investigations of human cognition and behavior in real-world contexts.

## Resources and Support

##### Code Repository

+ [Useful Functions](https://github.com/julianreiser/mbt-Conference-3.0-Workshop/tree/main/functions) - Complete collection of analysis functions used in this workshop
+ [BeMoBIL Pipeline](https://github.com/BeMoBIL/bemobil-pipeline) - Standardized mobile brain/body imaging preprocessing

##### Documentation

+ [LSL Documentation](https://labstreaminglayer.readthedocs.io/) - Comprehensive guide to Lab Streaming Layer
+ [EEGLAB Tutorial](https://eeglab.org/tutorials/) - Official EEGLAB documentation and tutorials

##### Contact and Support

+ **Workshop Instructors:**
  - Melanie Klapprott (Carl von Ossietzky University Oldenburg)
  - Emma Lieker (Leibniz Research Centre for Working Environment and Human Factors)  
  - Julian Elias Reiser (Leibniz Research Centre for Working Environment and Human Factors)

+ **Follow-up Presentations:**
  - Tuesday 10:30 - "Walking and Cognitive Load: Neural and Behavioral Responses in Virtual Environments"
  - Tuesday 10:45 - "Neurocognitive Effects of Physical Exercise and Mobile EEG"
  - Monday 16:15 - "EEGManySteps: Collaborative Data Collection and Analysis"