# YouTube Comments Scraper
![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Selenium](https://img.shields.io/badge/Selenium-4.0%2B-orange)
![License](https://img.shields.io/badge/License-MIT-green)

A Python-based tool to scrape comments from YouTube videos using **Selenium**. This script extracts comments and their authors from a specified YouTube video and saves the data in a CSV file. It handles pagination and avoids duplicates, making it efficient for large-scale comment scraping.

![YouTube Comments Scraper Demo](13.02.2025_13.35.07_REC-ezgif.com-video-to-gif-converter.gif)

---

## Table of Contents
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Output](#output)

---

## Features
- **Scrape Comments**: Extract comments and their authors from YouTube videos.
- **Pagination Handling**: Automatically scrolls to load more comments.
- **Duplicate Prevention**: Ensures no duplicate comments are saved.
- **CSV Export**: Saves scraped data in a CSV file with UTF-8 encoding for proper emoji display.
- **Customizable**: Easily adjust the number of comments to scrape or retry logic.

---

## Installation
Ensure you have Python installed, then install the required dependencies:
```bash
pip install -r requirements.txt
```
### Prerequisites
- Python 3.8 or higher.
- Google Chrome browser.
- ChromeDriver (matching your Chrome version).

## Usage

### Running the Script
To scrape YouTube comments, run the script with the required parameters:
```bash
python scrape_comments.py --video_id VIDEO_ID --output output.json
```

### Arguments
- `--video_id`: The ID of the YouTube video from which comments will be scraped.
- `--output`: (Optional) The name of the output file where scraped comments will be saved. Default is `comments.json`.

### Example Usage
```bash
python scrape_comments.py --video_id dQw4w9WgXcQ --output comments.json
```

### Notes
- Ensure you have a valid YouTube API key if required.
- The script may require authentication depending on the scraping method used.
- Handle API rate limits if using YouTube Data API.

### Troubleshooting
If you encounter issues, consider:
- Checking your API key and quota.
- Ensuring the video ID is correct and the video has public comments.
- Running the script with appropriate permissions if encountering access errors.

For more details, refer to the project documentation or raise an issue in the reposito
## Output
![CSV Output Screenshot](Screenshot-2025-02-13-40120.png)


The script generates a CSV file (`Comment.csv`) with the following columns:
- **Author**: The username of the commenter.
- **Comment**: The text of the comment.

### Example Output in Markdown Table Format

| Author       | Comment                     |
|--------------|-----------------------------|
| JohnDoe      | Great video!                |
| JaneSmith    | Thanks for the tutorial.    |
| Alice        | This was very helpful.      |
| Bob          | Can you make more of these? |