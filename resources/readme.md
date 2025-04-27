# PDF to Podcast: A Step-by-Step Guide using AI

This repository provides a comprehensive guide to **converting a PDF document into a podcast** using **AI-powered tools**.

---

## 📚 Overview

We follow these steps:

1. **Load and Preprocess PDF**  
   Extract text, create chunks, and prepare data for processing.
2. **Clean and Summarize Chunks**  
   Refine extracted text using the **Llama model** with custom prompts.
3. **Generate Podcast Script**  
   Craft a dialogue between two speakers based on the processed data.
4. **Make Script Dramatic**  
   Add impressions and enhance the engagement of the script.
5. **Convert Script to Audio**  
   Use text-to-speech models like **Parler-TTS** and **Bark** to generate audio.
6. **Generate Podcast Video** (Final Step)  
   Take the podcast transcript and audio to create a video using the **Wan2.1 1.3B model**.

---

# 🎥 Generate Podcast Video from Transcript — V1 (Final Step)

## Overview

This notebook outlines the final step in generating a podcast video from a PDF document.  
It takes the **podcast transcript** and **audio** generated in previous steps, and creates a **video**.

- **Last Step**: Part of the "**Generate Podcast from PDF V1**" series.
- **Model Used**: `Wan2.1 1.3B` from [Wan-AI](https://huggingface.co/Wan-AI).
- **Data Needed**:
  - Podcast transcript
  - Podcast audio
- **Prompt Engine**: Uses **Langchain** and **Groq** for prompt generation.
- **GPU Requirement**:  
  Designed for **A100 (40GB RAM)**.  
  Works (with tuning) on **Colab Pro T4 (24GB RAM)**.

---

## 🚀 Steps

1. **Install Libraries**  
   Install `diffusers`, `moviepy`, `langchain-groq`, and others.

2. **Load Data**  
   Load the podcast transcript and audio data.

3. **Prompt Generation**  
   Use Langchain + Groq to generate **creative prompts** for video generation.

4. **Video Generation**  
   Utilize **Wan2.1 1.3B** with generated prompts to create video clips.

5. **Combine Clips**  
   Merge the individual video clips and audio to create the final podcast video.

---

## 🔑 Usage

- Provide the paths to your podcast transcript and audio files.
- Set your Groq API key:

```python
from google.colab import userdata
userdata.set("grpq", "YOUR_API_KEY")
```

- Execute the notebook cells to generate the podcast video.

---

## 📝 Notes

- **Enable GPU** acceleration in Colab.
- Adjust video parameters (`height`, `width`, `guidance_scale`) as needed.
- A **checkpoint system** is included to **resume generation** if interrupted.

---

## 📈 TODO

- **Fine-tune Prompts**:  
  Improve video generation by experimenting with detailed descriptions, emotions, camera angles.

- **Incorporate PDF Content**:  
  Include images or more contextual visuals from the original PDF into the final video.

- **Explore Other Models**:  
  Compare output quality with models like **Lightricks/LTX-Video**.

- **Create a Complete Pipeline**:  
  Build an end-to-end pipeline from **PDF input → Final Podcast Video**.

- **Develop API or Gradio App**:  
  Make the tool accessible to non-coders through a web interface.

---

## 📚 References

- [Llama Recipes](https://github.com/facebookresearch/llama-recipes) — Inspiration for transcript cleaning and summarization techniques.
- [Wan-AI](https://huggingface.co/Wan-AI) — Used Wan2.1 1.3B model for text-to-video generation.

---

# 📣 Conclusion

This project demonstrates how to generate **podcast videos from PDF documents** using cutting-edge AI models.  
Future improvements can enhance creativity, flexibility, and make the system more accessible to a broader audience!
