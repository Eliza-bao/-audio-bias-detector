# -audio-bias-detector
# Audio Bias Detector

This project implements an AI-powered audio analysis pipeline designed to detect harmful or biased speech in media content. Built using OpenAI's Whisper for speech-to-text transcription and RoBERTa-based models for text classification, the tool supports ethical media reporting by identifying xenophobic language, misinformation, and toxic narratives in podcasts, interviews, and broadcast content.

## Project Objectives

- Transcribe spoken-word audio into structured text
- Detect biased or harmful content (e.g., identity hate, threats, toxicity)
- Provide explainable output for moderation and accountability
- Support real-time or batch analysis of media speech content

##  Tools and Technologies

- [Whisper](https://github.com/openai/whisper) – Automatic speech recognition
- [Hugging Face Transformers](https://huggingface.co/docs/transformers/index) – RoBERTa/Unitary models for classification
- Python, PyTorch, Pandas, CSV/JSON processing

## 📁 Repository Structure
├── src/ # Python scripts for transcription and classification │ ├── whisper_transcribe.py │ ├── classify_bias.py │ └── utils.py ├── toxic_dataset/ # Sample labeled dataset for testing/demo │ └── sample_data.csv ├── results.csv # Sample output (transcript + prediction) ├── requirements.txt # Python dependencies ├── README.md # Project documentation

## 🚀 How to Run

```bash
# Step 1: Set up environment
pip install -r requirements.txt

# Step 2: Run Whisper transcription
python src/whisper_transcribe.py --input sample.wav --output transcript.txt

# Step 3: Run text classification
python src/classify_bias.py --input transcript.txt --output results.csv

