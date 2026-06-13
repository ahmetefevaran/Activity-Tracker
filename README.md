# Activity-Tracker

A person activity recognition pipeline that detects and tracks multiple people across video frames, classifies their activity, and presents results through an interactive web interface.

What it does


Detects people in each frame using YOLOv8
Tracks them across frames using DeepSORT, maintaining consistent IDs even after occlusion
Re-identifies the same person using TorchReID when they re-enter the frame
Classifies activity (sitting, standing, walking) using pose-based heuristics
Supports different environment presets (office, cafe, market)
Optionally restricts analysis to a specific region of the frame (ROI)
Provides a Gradio web interface with live frame preview and per-person activity report


Tech Stack

Python, OpenCV, YOLOv8, DeepSORT, TorchReID, Gradio

Usage

Open the notebook in Google Colab, set your frames directory, and launch the Gradio interface. Configure the environment, frame interval, similarity thresholds, and optionally a ROI. Click start to begin analysis.

Input should be pre-extracted frames (JPEG/PNG). GPU runtime recommended for reasonable speed.
