# Running TutorGPT

TutorGPT is an AI assistant meant to act like a TA helping students better understand course material. It is built using the OpenAI API, using prompt engineering and an alternate interface to force more cognitive engagement. Students can upload class notes to TutorGPT, which the bot will reference when answering questions. TutorGPT is designed to provide hints that help to answer the questions, but not to answer the full questions themselves. In initial testing, students using this interface engaged more with their course material and were less likely to copy and paste full questions to ask the AI assistant.

## Installations

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

Running the server will require the following installations:
```
npm install openai
npm install dotenv
npm install express multer
```

## Running locally
Run this in the my-tutor directory. Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.
```
npm start
```

Run this in the server directory
```
node server.mjs
```


## OpenAI API key and Assistant configuration
This web app uses the OpenAI API to make calls to gpt-3.5-turbo-1106, as well as the Assistants API (currently in Beta). 
You'll need to add a .env file in the server folder. In this file include:
```
OPENAI_KEY=...
assistant_id=...
```
You can get an OpenAI API key by creating an account, going to API keys, and creating a new secret key. Copy and paste that into the .env file for OPENAI_KEY.

The assistant_id is the ID fo the assistant you create, using the Assistants API. To create an Assistant, run:
```
create_assistant()
```
in the openai.mjs directory. This will create an assistant with unique prompting instructions, and will print the ID of that assistant to the console. Copy that ID into assistant_id in the .env file.
