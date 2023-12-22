# Dialogflow-Misha-Chatbot

## Developing a basic Dialogflow chatbot

### How to Run:

1. Open the project's root folder "Dialogflow-Misha-Chatbot"
2. Create a virtual environment:
   ```bash
   python -m venv chat_venv
   ```
3. Activate the virtual environment:
   - On Windows:
     ```bash
     .\chat_venv\Scripts\activate
     ```
   - On macOS and Linux:
     ```bash
     source chat_venv/bin/activate
     ```
4. Install the following dependencies:
   ```bash
   pip install mysql-connector-python
   pip install fastapi[all]
   ```
5. Run the back-end:
   ```bash
   uvicorn main:app --reload
   ```
6. Open the `home.html` file in the frontend folder.

### How to Configure the Chatbot:

1. Create the chatbot in Dialogflow or use the Misha chatbot at the following link:
   [Dialogflow Misha Chatbot](https://console.dialogflow.com/api-client/demo/embedded/abb5b2ae-c8fb-48f2-8eb3-a3bf40669ded)

2. Update the link in the `frontend folder/home.html`

3. Download ngrok for https connection on your computer at the following link:
   [Ngrok Download](https://ngrok.com/download)

4. Upon downloading, extract the `ngrok.exe` file and place it in the root folder

5. In an alternative terminal (not the one your back-end is running in), activate the https connection:
   ```bash
   ngrok http <port number>
   ```

(This port number can be seen when you run the back-end)

6. Put the URL given into the Dialogflow configuration
   i. Navigate to Fulfillment
   ii. Enable Webhook
   iii. Add the URL into the URL section
   iv. Click Save
