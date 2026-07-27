# Running a Free Streamlit Demo Locally

Follow these steps to set up and run this app's Streamlit demo on your own laptop, completely free.

## 1. Prerequisites
- Python 3.9+ installed (check with `python --version`)
- Git installed
- (Optional) A code editor like VS Code

## 2. Clone the Repository
```
git clone https://github.com/yerra-srikar/reverse-tutor.git
cd reverse-tutor
```

## 3. Create a Virtual Environment
```
python -m venv venv
```
Activate it:
- Windows: `venv\Scripts\activate`
- macOS/Linux: `source venv/bin/activate`

## 4. Install Dependencies
If a `requirements.txt` exists:
```
pip install -r requirements.txt
```
Otherwise, install Streamlit directly:
```
pip install streamlit
```

## 5. Add Environment Variables (if needed)
If the app uses API keys (e.g., Gemini, OpenAI), create a `.env` file or a `.streamlit/secrets.toml` file:
```
# .streamlit/secrets.toml
API_KEY = "your-api-key-here"
```
Never commit this file to GitHub.

## 6. Run the App
```
streamlit run app.py
```
Replace `app.py` with the actual entry-point script name in this repo.

## 7. View the Demo
Streamlit will automatically open a browser tab at:
```
http://localhost:8501
```
If it doesn't open automatically, copy the URL from the terminal into your browser.

## 8. Stopping the App
Press `Ctrl + C` in the terminal to stop the local server.

## 9. (Optional) Free Public Hosting
To share the demo online for free without using your laptop as a server:
1. Push your code to GitHub.
2. Go to https://share.streamlit.io
3. Sign in with GitHub and click "New app".
4. Select this repository, branch, and entry-point file.
5. Add any secrets under "Advanced settings".
6. Click "Deploy" — you'll get a free public URL.

## Troubleshooting
- `ModuleNotFoundError`: Run `pip install -r requirements.txt` again inside the activated venv.
- Port already in use: Run `streamlit run app.py --server.port 8502`.
- Changes not reflecting: Save the file and Streamlit will auto-reload, or press `R` in the browser.
