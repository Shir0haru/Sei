# Sei Chatbot

Sei is an Open-Source Serverless AI Chatbot Written in JavaScript, Using the Google Gemini API, and Deployed on Netlify.

<p align="center">
<img src="https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E">
<img src="https://img.shields.io/badge/google%20gemini-8E75B2?style=for-the-badge&logo=google%20gemini&logoColor=white">
<img src="https://img.shields.io/badge/netlify-%23000000.svg?style=for-the-badge&logo=netlify&logoColor=#00C7B7">
<img src="https://img.shields.io/badge/deno%20js-000000?style=for-the-badge&logo=deno&logoColor=white">
</p>

## Deployment

Here is the steps of deploying your Telegram Bot.
1. Create your Telegram Bot at [BotFather](https://t.me/@BotFather). You'll be given an API Key for your Bot. You'll need it later.
2. Create your Google Gemini API at [Google AI Studio](https://aistudio.google.com/api-keys).
3. After doing step 1 and 2, you should have something similarly like this. Save them as ``.env``. Do Not expose these into Public.
```env
TELEGRAM_API_KEY="6819473025:392aAca66920E474Bb82461A706e6800"
GEMINI_API_KEY="AIzaSyB7ff1818c62D9d53b601076E89b51fC4"
```
Warning! These API Key is fake. You need to use your actual API key from Telegram and Gemini. Insert it between the bracket.

4. [Fork](https://github.com/Shir0haru/Sei/fork) this Repository.
5. Take a look on the main code. The structure should be like this
```
Sei/
├── netlify/
│   └── edge-functions/
│       └── index.js      <--- Main Code
├── LICENSE
├── netlify.toml
└── package.json
```
Modify the pre-determined prompt if needed. You can change the AI name as you wish and how it behaves.

6. After doing the modification you desires, it's time to deploy it. We're gonna deploy it on Netlify. If you already had Netlify account, you can skip step 7 and 8.
7. Create your Netlify account [here](https://app.netlify.com/signup).
8. Confirm your Email to finishes your account creation on Netlify.
9. On Netlify, go to "Add New Project", then chooses "Import an existing project".
10. You'll be redirected, then, you'll need to choose between 4 Git Providers. Choose GitHub.
11. You'll be listed all your repository. Choose this forked repository.
12. Scroll Down and you'll see "Environment Variables". Click it and choose "Import from a .env file". Then choose the ``.env`` file you've saved earlier on Step 3.
13. Only then, you can deploy. But the job isn't finished yet. You need to add webhook to the Telegram Bot. And it's quite simple.
14. To add Webhook to Telegram Bot, you need to obtain the project domain, which you'll get after deploying. It should be look similarly like this:
```
sei-chatbot.netlify.app
```
15. Set the Webhook by input these to your web browser:
```
https://api.telegram.org/bot6819473025:392aAca66920E474Bb82461A706e6800/setWebhook?url=https://sei-chatbot.netlify.app/api/interactions
```
Again, the Token is fake, you need to use your actual token. Insert your token after the word ``/bot`` without spaces.

16. Done. Congratulations. You just deployed your Serverless AI Chatbot. Enjoy!

## Screenshots

![App Screenshot](https://files.catbox.moe/gwlq0u.png)