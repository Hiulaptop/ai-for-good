# Psychological Counseling Chatbot

This is a simple web-based chatbot designed to provide psychological counseling using the Gemini API. The service is delivered directly to users without requiring any login, and all chat data is ephemeral, disappearing on page reload.

## Features

*   **Text-to-Text Counseling:** Provides psychological counseling through text-based conversations.
*   **Gemini API Integration:** Utilizes the `gemini-2.0-flash-lite` model for generating responses.
*   **No Login Required:** Accessible directly via URL.
*   **Ephemeral Sessions:** No data is stored; everything resets on page reload.
*   **Visually Appealing Interface:** Designed with a calming color scheme and engaging effects suitable for mental health and wellbeing.
*   **Typing Indicator:** Shows a "..." animation when the chatbot is generating a response.
*   **Customizable System Prompt:** Easily modify the chatbot's persona and guidance.

## Setup Instructions

Follow these steps to get the chatbot up and running on your local machine.

### Prerequisites

*   Python 3.8+
*   `pip` (Python package installer)

### 1. Clone the Repository (if applicable)

If you received these files as a package, skip this step. Otherwise, clone the repository:

```bash
git clone [repository-url]
cd [repository-directory]
```

### 2. Install Dependencies

Navigate to the project's root directory and install the required Python packages:

```bash
pip install -r requirements.txt
```

### 3. Configure Gemini API Key

You need a Gemini API key to run this application.
1.  Obtain your API key from the [Google AI Studio](https://aistudio.google.com/app/apikey).
2.  Create a file named `.env` in the root directory of this project (the same directory as `main.py`).
3.  Add your API key to the `.env` file in the following format:

    ```
    GEMINI_API_KEY=YOUR_API_KEY_HERE
    ```
    Replace `YOUR_API_KEY_HERE` with your actual Gemini API key.

### 4. Customize the System Prompt (Optional)

You can guide the chatbot's behavior by modifying the `SYSTEM_PROMPT` in `main.py`. Open `main.py` and edit the `SYSTEM_PROMPT` variable:

```python
# Placeholder for the system prompt
SYSTEM_PROMPT = """
You are a helpful psychological counselor. Your goal is to provide supportive and empathetic guidance.
"""
```
Adjust the text within the triple quotes to define the chatbot's persona and instructions.

## Running the Application

Once the setup is complete, you can start the Flask development server:

```bash
python main.py
```

The application will typically run on `http://127.0.0.1:5000/`. Open this URL in your web browser to access the chatbot.

## Usage

*   Upon visiting the URL, a chat window will automatically appear with an initial greeting from the bot.
*   Type your message in the input field and press Enter or click the "Send" button.
*   The chatbot will respond, and a typing indicator will show when it's generating a reply.
*   Refreshing the page will clear the conversation history.
