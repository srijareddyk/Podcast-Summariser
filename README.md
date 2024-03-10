# Podcast-Summariser

## Executive Summary

The Podcast Summarizer project aims to develop a robust solution for condensing lengthy podcast episodes into shorter, engaging summaries. The motivation behind this initiative is to enhance the accessibility of podcast content, providing listeners with concise, informative summaries that capture the essence of the episodes. The project utilizes a combination of speech-to-text models for transcribing audio and transformer-based summarization models for generating concise summaries.

## Problem Definition

Podcasts have gained immense popularity, offering diverse content across various topics. However, lengthy episodes can be time-consuming and may deter listeners. The goal of this project is to address this issue by creating an automated system that extracts valuable insights from podcasts and presents them in a condensed format.

## Implementation

### Audio to Text Model (Speech-to-Text)

The team used the SpeechRecognition library to convert audio files into text, utilizing Google Web Speech APIs. The implementation includes handling ambient noise, recording audio, and recognizing speech, with error handling for API-related issues.

### Podcast Segmentation

The Pydub library was employed to segment large audio files into smaller, more manageable chunks. The script reads audio files, applies speech recognition to convert them into text, and writes the recognized text to a file named "mytxt.txt." Timestamps are extracted from filenames for further processing.

### Summarization Model

The summarization script utilizes the Hugging Face Transformers library to create a summarization pipeline. The chosen model, 'sshleifer/distilbart-cnn-12-6,' generates summaries for input text, which are then saved to a new text file.

## Evaluation

Employed the ROUGE package for evaluating the accuracy of the summarization model. ROUGE metrics, including precision, recall, and F1 scores, were calculated by comparing system-generated summaries to reference summaries. The results provide insights into the model's performance, highlighting areas for improvement.

## Results and Discussion

The project successfully demonstrated the integration of speech-to-text and summarization models for podcast summarization. The ROUGE scores indicated moderate overlap for unigrams but suggested room for improvement, especially concerning bigrams. The findings offer valuable insights for refining the summarization algorithm to enhance overall performance.

## Conclusion

The Podcast Summarizer project addresses the need for concise podcast summaries, catering to listeners' preferences for shorter, informative content. The team's collaborative efforts in implementing speech-to-text and summarization models, coupled with rigorous evaluation using the ROUGE metric, lay the foundation for future enhancements and widespread use.

---
