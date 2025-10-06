# YouTube Transcript Summarizer

A Python script that fetches the transcript of any YouTube video and uses the Google Gemini API to generate a concise summary.

-----

## About The Project

This project provides a simple, automated way to get the key points from a YouTube video without watching it. It uses the `youtube-transcript-api` library to extract the full transcript and then calls the Google Gemini API (via its OpenAI-compatible endpoint) to summarize the text.

The script is designed to handle potential issues like long transcripts by truncating the text to fit within the model's token limits.

-----

## Getting Started

Follow these steps to get the script running.

### Prerequisites

You will need a Google Gemini API key.

  * Get your key from [Google AI Studio](https://aistudio.google.com/app/apikey).

### Installation

1.  Clone this repository (or just download the script).
2.  Install the required Python packages:
    ```sh
    pip install youtube-transcript-api openai python-dotenv
    ```

### Configuration

1.  Create a file named `.env` in the same directory as the script.
2.  Add your API key to the `.env` file:
    ```
    GEMINI_API_KEY="YOUR_API_KEY_HERE"
    ```
3.  **For Google Colab users**: Instead of a `.env` file, it is highly recommended to use the **Secrets Manager** (🔑 icon) to store your API key with the name `GEMINI_API_KEY`.

-----

## Usage

1.  Open the Python script.
2.  Change the `video_url` variable to the YouTube video you want to summarize:
    ```python
    video_url = "https://www.youtube.com/watch?v=dQw4w9WgXcQ"
    ```
3.  Run the script from your terminal:
    ```sh
    python your_script_name.py
    ```
4.  The summary will be printed to the console.
