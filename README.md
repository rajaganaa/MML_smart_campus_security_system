<div align="center">
  
# 🛡️ Multimodal Smart Campus Security System

**An AI-driven, multimodal campus surveillance and threat detection framework leveraging Vision-Language Models (CLIP, BLIP) and Voice Biometrics.**

![Python](https://img.shields.io/badge/Python-3.8+-blue?style=for-the-badge&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![OpenAI CLIP](https://img.shields.io/badge/OpenAI_CLIP-412991?style=for-the-badge&logo=openai&logoColor=white)
![Salesforce BLIP](https://img.shields.io/badge/Salesforce_BLIP-00A1E0?style=for-the-badge&logo=salesforce&logoColor=white)
![Status](https://img.shields.io/badge/Status-Active-success?style=for-the-badge)

</div>

---

## 📊 Business Use Case

In an era where campus security is paramount, relying solely on human monitoring for hundreds of CCTV feeds is inefficient and prone to error. **This application solves the problem of manual security surveillance** by utilizing advanced Multimodal Machine Learning. 

By combining visual scene understanding (BLIP), zero-shot anomaly classification (CLIP), facial recognition, and voice biometrics, the system acts as an autonomous, intelligent watchguard. It can detect unauthorized personnel, recognize enrolled individuals (like students and staff), and identify high-risk anomalies (e.g., weapons, fights, or unauthorized access) in real-time, instantly notifying administrators with rich contextual scene captions.

---

## ✨ Key Features

- **👁️ Vision-Language Scene Analysis**: Utilizes **Salesforce BLIP** to automatically generate natural language descriptions of CCTV frames, identifying complex scenarios.
- **🎯 Zero-Shot Anomaly Detection**: Leverages **OpenAI CLIP** to calculate similarity matrices between video frames and high-risk text prompts (e.g., "person holding weapon", "unauthorized entry").
- **👤 Multimodal Identity Verification**: 
  - Cross-references facial embeddings against an enrolled database.
  - Matches voice biometric audio streams to correctly identify individuals (e.g., *virat.wav*, *dhoni.wav*).
- **🚨 Automated Alerting System**: Distributes contextual alerts based on threat probability scores.

---

## 📂 Project Structure

```text
MML_smart_campus_security/
├── project_data/            
│   ├── enrolled/            # Enrolled personnel face images for verification
│   └── enrolled_audio/      # Registered voice biometrics (.wav files)
├── project_results/         
│   ├── alert_distribution.png       # Threat level analytics and chart
│   ├── blip_attention.png           # BLIP vision-text attention maps
│   ├── clip_bar_charts.png          # CLIP zero-shot confidence metrics
│   ├── enrolled_faces.png           # Processed face embeddings visualization
│   └── scene_captions.png           # Generated contextual scene alerts
├── Smart_Campus_Security.ipynb      # Main Multimodal ML execution pipeline
└── .gitignore                       # Git ignore configurations (ignoring large models/data)
```

---

## 🚀 Execution Pipeline

1. **Data Ingestion**: Takes in multimodal feeds (visual frames + audio clips).
2. **Feature Extraction**: 
   - Faces are cropped and transformed into latent embeddings.
   - Images are encoded via the CLIP Vision Transformer.
   - Audio is mapped to spectrograms/MFCCs.
3. **Fusion & Inference**: Combining Face Match + Voice Match + CLIP Similarity.
4. **Context Generation**: BLIP generates a human-readable caption.
5. **Alerting**: High-risk scenarios trigger an alert, saving visualizations into `project_results/`.

---

## 💻 Tech Stack & Libraries

* **Core ML**: `PyTorch`, `Transformers` (Hugging Face)
* **Vision Models**: `CLIP` (OpenAI), `BLIP`
* **Audio Processing**: `librosa`, `soundfile`
* **Computer Vision**: `OpenCV`, `facenet-pytorch`
* **Metrics/Visualization**: `matplotlib`, `seaborn`, `numpy`, `pandas`

---

## 🔧 Installation & Usage

**1. Clone the repository**
```bash
git clone https://github.com/rajaganaa/MML_smart_campus_security_system.git
cd MML_smart_campus_security_system
```

**2. Install Dependencies**
Ensure you have Python 3.8+ installed.
```bash
pip install torch torchvision torchaudio
pip install transformers opencv-python librosa matplotlib seaborn facenet-pytorch
```

**3. Run the Pipeline**
Launch Jupyter Notebook or JupyterLab and execute the main pipeline:
```bash
jupyter notebook Smart_Campus_Security_21AIE541T.ipynb
```
Follow the sequentially ordered cells to load the models, enroll the identities from `project_data/`, and process the simulated security inputs.

---

<div align="center">
  <b>Built with ❤️ for advanced campus security solutions by Rajaganapathy M</b>
</div>