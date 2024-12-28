Here’s the updated `README.md` file with all dependencies mentioned explicitly:  

```markdown
# Gemini Websocket and TTS Integration

This project integrates the Gemini AI API with a WebSocket server for real-time interactions. It also incorporates text-to-speech (TTS) functionality using `pyttsx3`.

---

## Features
- Real-time interaction with the Gemini AI API.
- Supports audio and image input for processing.
- Converts Gemini's text responses into speech using TTS (`pyttsx3`).
- Serves a basic HTTP server for additional client-side interactions.

---

## Dependencies

The following dependencies are required for this project:

| Dependency            | Version | Purpose                                                                 |
|-----------------------|---------|-------------------------------------------------------------------------|
| `google-genai`        | 0.2.2   | To interact with the Gemini AI API.                                    |
| `pyttsx3`             | Latest  | Provides text-to-speech functionality.                                 |
| `websockets`          | Latest  | Enables WebSocket communication.                                       |
| `asyncio`             | Built-in | Provides asynchronous programming support.                             |
| `json`                | Built-in | For handling JSON messages.                                           |
| `os`                  | Built-in | To manage environment variables and paths.                            |
| `base64`              | Built-in | To encode and decode media data for transmission.                     |

---

## Setup Instructions

### 1. Clone the Repository
```bash
git clone <repository-url>
cd <repository-folder>
```

### 2. Create and Activate a Virtual Environment
```bash
python -m venv venv
# Activate on Windows
venv\Scripts\activate
# Activate on Linux/Mac
source venv/bin/activate
```

### 3. Install Required Dependencies
```bash
pip install --upgrade pip
pip install pyttsx3 google-genai==0.2.2 websockets
```

---

## Running the Project

### Step 1: Start the WebSocket Server
Run the main Python script to start the WebSocket server:
```bash
python main2.py
```

The server will run on `localhost:9080`.

### Step 2: Serve a Static HTTP Server (Optional)
If you need to serve additional client-side files, run:
```bash
python -m http.server
```

The HTTP server will run on `localhost:8000`.

---

## Configuration

### Environment Variables
Add the following to your environment variables to authenticate with the Gemini API:
```bash
export GOOGLE_API_KEY="YOUR_GOOGLE_API_KEY"
```
Replace `"YOUR_GOOGLE_API_KEY"` with your actual API key.

### Model Configuration
Modify the model configuration in the `main2.py` file as needed:
```python
MODEL = "gemini-2.0-flash-exp"  # Update to your model ID
```

---

## Project Structure
```plaintext
project-folder/
│
├── main2.py        # Main server script
├── requirements.txt # (Optional) Add your dependencies for easy installation
├── README.md       # Project documentation
└── other_files/    # (Optional) Additional assets or scripts
```

---

## Notes
- Ensure your `GOOGLE_API_KEY` is valid and configured correctly.
- If additional dependencies are added, update `requirements.txt` using:
  ```bash
  pip freeze > requirements.txt
  ```

---

## Contributing
Feel free to fork this repository and submit pull requests for improvements or new features.

---

## License
This project is open-source and available under the [MIT License](LICENSE).
```

If you need more customization or would like me to generate the `requirements.txt` file directly, let me know!
