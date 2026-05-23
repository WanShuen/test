# 🎤 Text to Speech Streamlit Application

A streamlined Streamlit application that converts user-inputted text to speech using Azure AI Speech SDK.

## Features

✨ **Key Features:**
- 📝 Simple text input interface
- 🎙️ Multiple voice options (English, Spanish, French, German)
- 🎚️ Adjustable speech rate
- 🔊 Real-time speech synthesis
- ⚙️ Easy configuration panel
- 🎨 Beautiful, user-friendly UI

## Prerequisites

- Python 3.8+
- Azure account with Speech resource
- API key and region from Azure Speech service

## Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/WanShuen/test.git
   cd test
   ```

2. **Create a virtual environment (optional but recommended):**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up Azure credentials:**
   - Copy `.env.example` to `.env`
   - Add your Azure Speech API key and region to `.env`

   ```bash
   cp .env.example .env
   ```

   Edit `.env` and add your credentials:
   ```
   SPEECH_KEY=your_api_key_here
   SPEECH_REGION=your_region_here
   ```

## Getting Azure Credentials

1. Go to [Azure Portal](https://portal.azure.com)
2. Create a new "Speech" resource
3. Once created, navigate to the resource
4. Copy your **API Key** and **Region** from the "Keys and Endpoint" section
5. Paste them into the `.env` file

## Running the Application

```bash
streamlit run app.py
```

The application will open in your browser at `http://localhost:8501`

## Usage

1. **Enter Text:** Type or paste your text in the text area
2. **Configure (Optional):** Use the sidebar to:
   - Enter your Azure Speech credentials (if not using .env)
   - Select a voice
   - Adjust speech rate
3. **Click "Speak":** The application will convert your text to speech and play it immediately
4. **Click "Clear":** Clear the text area for new input

## Available Voices

- 🇺🇸 English (US) - Male & Female
- 🇬🇧 English (UK) - Male & Female
- 🇪🇸 Spanish
- 🇫🇷 French
- 🇩🇪 German

## Architecture

```
app.py
├── Streamlit UI Components
├── Azure Speech SDK Integration
├── Environment Configuration
└── Error Handling
```

## Troubleshooting

**Issue:** "Azure credentials not configured"
- Solution: Ensure `.env` file exists with valid `SPEECH_KEY` and `SPEECH_REGION`

**Issue:** "No sound output"
- Solution: Check system volume and speaker settings
- Ensure your Azure API key is valid

**Issue:** "Invalid API key"
- Solution: Verify your key in Azure Portal
- Make sure the key matches the correct Speech resource region

## Environment Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `SPEECH_KEY` | Azure Speech API Key | `abc123...` |
| `SPEECH_REGION` | Azure region | `eastus`, `westus` |

## Dependencies

- **streamlit**: Web app framework
- **azure-cognitiveservices-speech**: Azure AI Speech SDK
- **python-dotenv**: Environment variable management

## License

MIT License - Feel free to use and modify this project

## Support

For issues with Azure Speech SDK, visit: https://github.com/Azure-Samples/cognitive-services-speech-sdk

---

Made with ❤️ using Streamlit & Azure AI Speech SDK
