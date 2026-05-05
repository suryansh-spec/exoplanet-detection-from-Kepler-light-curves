🚀 Exoplanet Detection using Deep Learning (Kepler Data)
🌌 Overview

This project explores an end-to-end pipeline for detecting exoplanet transits from stellar light curve data obtained from NASA’s Kepler mission. It combines astrophysical signal processing with deep learning (1D CNNs) to identify periodic dips in brightness caused by orbiting planets.

Unlike toy ML problems, this project deals with noisy, real-world time-series data, where meaningful patterns are subtle and heavily masked by stellar variability.

🧠 Key Idea

When a planet passes in front of a star, it causes a small, periodic drop in brightness (transit).

The goal:

Learn to detect these patterns automatically using deep learning.

⚙️ Pipeline
1. Data Preprocessing
Detrending using polynomial fitting
Noise reduction and normalization
Conversion of continuous signal into sliding windows
2. Signal Analysis
Lomb-Scargle Periodogram for periodicity detection
Heuristic-based identification of potential transit regions
3. Model Architecture
1D Convolutional Neural Network (Conv1D)
Captures local temporal patterns in flux variations
Designed for time-series classification
4. Training & Evaluation
Train-test split on processed segments
Performance evaluation using classification metrics
Visualization of predicted transit signals
📊 Why This is Interesting
Works on astronomical time-series data, not standard datasets
Combines classical signal processing + deep learning
Tackles a low signal-to-noise problem, similar to real-world ML systems
Demonstrates how ML can assist in scientific discovery
🧪 Current Limitations
Labels are partially heuristic-based (not fully ground-truth validated)
Limited benchmarking against classical methods
Not optimized for production-scale inference
🔮 Future Improvements
Use confirmed Kepler exoplanet labels for supervised learning
Compare against classical transit detection methods
Experiment with LSTM / Transformer architectures
Improve evaluation metrics (Precision, Recall, F1, ROC)
Build a real-time inference or visualization tool
🛠️ Tech Stack
Python
NumPy, Pandas
Matplotlib
Scikit-learn
TensorFlow / Keras
📌 Takeaway

This project demonstrates how deep learning can be applied beyond standard benchmarks to complex, noisy scientific data, bridging the gap between machine learning and astrophysics.
