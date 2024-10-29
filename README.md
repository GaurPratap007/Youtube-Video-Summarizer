# YouTube Video Summarizer

This Python program automates the process of summarizing YouTube videos. Given a YouTube video URL, it extracts the video ID, retrieves the video transcript using the YouTube Transcript API, and generates a concise summary using Google’s Gemini API.

## Features

- **Video ID Extraction**: Extracts video ID from a YouTube link using regular expressions.
- **Transcript Retrieval**: Fetches transcript of the video using the YouTube Transcript API.
- **Automatic Summarization**: Uses Google’s Gemini AI model to generate a concise summary of the transcript.

## Requirements

- Python 3.7 or higher
- Required packages:
  - `google-generativeai`
  - `youtube-transcript-api`

Install required packages using:

```bash
pip install google-generativeai youtube-transcript-api
```

## Setup

1. **Clone this repository**:
    ```bash
    git clone https://github.com/your-username/Youtube-Video-Summarizer.git
    cd Youtube-Video-Summarizer
    ```

2. **Set up Google Gemini API Key**:
   - Set up an environment variable for your Google API key, or replace `os.environ["API_KEY"]` in the code with your actual API key.

   **For Environment Variable Setup**:
   ```bash
   export API_KEY="your_actual_api_key"
   ```

3. **Run the Program**:
   Update the `youtube_url` variable in the script with a YouTube video link and run:

   ```bash
   python summarizer.py
   ```

## Usage Example

```python
youtube_url = "https://www.youtube.com/watch?v=your_video_id"
summary = summarize_youtube_video(youtube_url)
print("Summary:", summary)
```

## Code Overview

- **`extract_video_id(url)`**: Extracts the video ID from a YouTube URL using regex.
- **`fetch_transcript(video_id)`**: Retrieves the transcript for the video ID using YouTube Transcript API.
- **`summarize_text(text)`**: Summarizes the transcript using the Gemini model.
- **`summarize_youtube_video(url)`**: Automates the entire summarization process for a YouTube URL.

## Troubleshooting

- **KeyError for API Key**: Ensure that the API key is correctly set up as an environment variable or hardcoded.
- **Transcript Not Available**: Some videos do not have transcripts. The program will return a message if a transcript is unavailable.

## Contributing

Contributions are welcome! Feel free to open issues or submit pull requests.
