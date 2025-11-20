# YouTube Comments Analyzer 🎥💬

A Streamlit web application that analyzes YouTube video comments and provides AI-powered insights using Google's Bard API. This tool helps content creators understand viewer feedback by extracting comments from any YouTube video and generating a comprehensive review summary.

## 🌟 Features

- **Extract YouTube Comments**: Retrieves all comments from any YouTube video using the YouTube Data API
- **AI-Powered Analysis**: Uses Google Bard AI to analyze and summarize comments
- **Video Information Display**: Shows video thumbnail, channel name, and other metadata
- **Interactive Web Interface**: Built with Streamlit for an easy-to-use experience
- **Comprehensive Review**: Generates a third-person review highlighting both positive and negative feedback

## 📋 Prerequisites

Before running this application, you need:

- Python 3.7 or higher
- YouTube Data API Key (v3)
- Google Bard API Key

## 🔧 Installation

1. Clone this repository:
```bash
git clone https://github.com/sanjithrj/Comments_Analysis.git
cd Comments_Analysis
```

2. Install the required dependencies:
```bash
pip install -r requirements.txt
```

Required packages (as listed in `Requirements` file):
- `google-api-python-client` (googleapiclient)
- `pandas`
- `streamlit`
- `bardapi`
- `requests`

## 🔑 Configuration

You need to configure two API keys in the `app.py` file:

### 1. YouTube Data API Key

1. Go to [Google Cloud Console](https://console.cloud.google.com/)
2. Create a new project or select an existing one
3. Enable the YouTube Data API v3
4. Create credentials (API Key)
5. Replace `"Youtube_api_key"` in `app.py` (line 13) with your actual API key:
```python
DEVELOPER_KEY = "your_youtube_api_key_here"
```

### 2. Bard API Key

1. Visit [Google Bard](https://bard.google.com/)
2. Get your Bard API key (instructions can be found in the [bardapi documentation](https://github.com/dsdanielpark/Bard-API))
3. Replace `"Bard_API_Key"` in `app.py` (line 100) with your actual API key:
```python
os.environ["_BARD_API_KEY"] = "your_bard_api_key_here"
```

## 🚀 Usage

1. Start the Streamlit application:
```bash
streamlit run app.py
```

2. Open your web browser and navigate to the provided local URL (typically `http://localhost:8501`)

3. Enter a YouTube video URL in the text input field

4. Click the "Analyse" button

5. The application will:
   - Display the video thumbnail
   - Show the channel name
   - Analyze the first 30 comments
   - Generate an AI-powered review summary

## 📁 Project Structure

```
Comments_Analysis/
│
├── app.py                      # Main Streamlit application
├── sentiment_analysis.ipynb    # Jupyter notebook for analysis experiments
├── Requirements                # List of required Python packages
└── README.md                   # This file
```

## 🛠️ Technologies Used

- **Streamlit**: Web application framework
- **YouTube Data API v3**: For fetching video comments and metadata
- **Google Bard API**: For AI-powered comment analysis
- **Pandas**: Data manipulation and analysis
- **Python Requests**: HTTP library for API calls

## 📝 How It Works

1. **Video ID Extraction**: Extracts the video ID from the provided YouTube URL
2. **Comment Retrieval**: Uses YouTube Data API to fetch all comments with pagination support
3. **Data Processing**: Stores comments in a Pandas DataFrame for easy manipulation
4. **AI Analysis**: Sends the first 30 comments to Google Bard for analysis
5. **Review Generation**: Bard generates a comprehensive review highlighting good and bad aspects
6. **Display Results**: Shows the analysis results with video thumbnail and channel information

## ⚠️ Important Notes

- The application analyzes only the first 30 comments due to API limitations and processing efficiency
- Make sure to keep your API keys secure and never commit them to version control
- The YouTube Data API has usage quotas; monitor your usage in the Google Cloud Console
- Ensure the video has comments enabled and is publicly accessible

## 🤝 Contributing

Contributions are welcome! Feel free to:
- Report bugs
- Suggest new features
- Submit pull requests

## 📄 License

This project is open-source and available for educational purposes.

## 👤 Author

**Sanjith RJ**
- GitHub: [@sanjithrj](https://github.com/sanjithrj)

## 🙏 Acknowledgments

- Google for YouTube Data API and Bard API
- Streamlit team for the amazing framework
- bardapi library developers

---

**Note**: Remember to replace the placeholder API keys with your actual keys before running the application!