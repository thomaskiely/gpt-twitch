# GPT-stream

A bot that can talk to twitch chat that leverages Chat GPT

# How to use

1. Create a .env file in the root directory with the following structure:

    OPENAI_API_KEY=
    TWITCH_TOKEN=
    TWITCH_CLIENT_ID=
    TWITCH_USERNAME=
    MIN_MESSAGE_LENGTH=

    Set the TWITCH_USERNAME field to your username and the MIN_MESSAGE_LENGTH field to the min characters a message should be for the bot to respond to.

2. Go to https://platform.openai.com/api-keys and generate a new api key, and set this to the value of OPENAI_API_KEY in your env file.

3. Go to https://platform.openai.com/settings/organization/billing/overview and add a credit balance for the bot to work.
    The model used for this bot is relatively cheap so you can start with only $5 and add more later if you need to.

4. Go to https://dev.twitch.tv/console and click 'Register Your Application'
    Fill in the Name of your app
    Under OAuth Redirect URL: Use http://localhost
    Under Category select Application Integration
    Under Client Type Select Confidential then press 'Create'
    Go into 'Manage' under your app and copy the client id
    Paste this value into TWITCH_CLIENT_ID in your env file

5. Go to https://twitchtokengenerator.com/ and choose Bot Chat Token
    Authorize your twitch channel and go through the CAPTCHA
    Copy down the 'Access Token' field and paste the value into the TWITCH_TOKEN field in your .env file

6. Add your prompt to the prompts.py file - the more context you give here, the better


7. Make sure you have python 3 installed and run 'python stream.py' in a terminal from the root directory and the bot will start


# Recommendations

1. Use a window capture on the pygame window that shows up and use a color key on the background color of the window

2. Feel free to change the images being used for notTalking.png and talking.png, just make sure you name them the same, or change the names in stream.py
