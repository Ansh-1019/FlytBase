# 🚨 Drone Video Anomaly Detection using Qwen2.5-VL

An AI-powered drone video anomaly detection system that uses a Vision-Language Model (VLM) to analyze surveillance videos, identify abnormal events, classify them into predefined categories, and generate competition-ready structured JSON predictions.

The project uses **Qwen2.5-VL-3B-Instruct** with **LoRA fine-tuning**, combined with efficient temporal frame sampling. Instead of processing every frame of a video, the system extracts **9 evenly spaced frames**, combines them into a **3×3 visual grid**, and provides the resulting image to the multimodal model for classification.

---

## 📌 Overview

Drone surveillance systems generate large amounts of video data. Continuously monitoring this footage manually is time-consuming and can result in important events being missed.

This project provides an automated solution for detecting anomalies in drone surveillance videos.

The system analyzes video clips and classifies them into 12 predefined categories, including traffic incidents, fire, smoke, suspicious activity, violence, flooding, and other road-related anomalies.

The overall pipeline is:

```text
Drone Video
     │
     ▼
Temporal Frame Sampling
     │
     ▼
9 Evenly Spaced Frames
     │
     ▼
3 × 3 Frame Grid
     │
     ▼
Qwen2.5-VL-3B-Instruct
     │
     ▼
LoRA Fine-Tuned Model
     │
     ▼
Anomaly Classification
     │
     ▼
Structured JSON
