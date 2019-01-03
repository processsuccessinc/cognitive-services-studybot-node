# Study Bot Node

This sample contains the Visual Studio Node/Express app that will embed the bot you created in the [qna-luis-botv4-node sample](https://github.com/Azure-Samples/cognitive-services-studybot-node/tree/master/qna-luis-botv4-node).

This app is a `Basic Node.js Express 4 Application` created in Visual Studio.

## Prerequisites

1. Build the [qna-luis-botv4-node sample](https://github.com/Azure-Samples/cognitive-services-studybot-node/tree/master/qna-luis-botv4-node) and make sure your local code has been published back to Azure.

1. Create a DirectLine channel in Azure, where your bot resource is located. To do this go to the Channels menu in your web app bot resource in Azure and click the globe icon.

    <img src="/Assets/enable-directline.png">
    
1. This initializes the Direct Line channel. A popup appears that has your bot secret key.

1.  Click "show" and copy the key (either key will work) to your clipboard. 
    
    <img src="/Assets/bot-secret-key.png">

1. Click "Done" at the bottom. Then you will see Direct Line has been added next to Web Chat.

    <img src="/Assets/directline-done.png">
    
1. Next, we will paste this secret key into this sample. Clone or download this repo, then go to the `cognitive-services-studybot-node/StudyBotNode/` folder and open the `StudyBotNode.sln` file.

1. In your `index.pug`, paste your copied DirectLine key where indicated in the WebChat script.


## Run and Test the sample

1. Run your StudyBotNode solution file in Visual Studio.

1. A browser window will open and you will see the app's interface.

1. Enter `hi` into the chat client. It might take a little time for the bot to warm up. If it fails to send, keep trying again, it should work.

1. Once you get a response from the bot, click the tabs below to see that the query has been captured and added to the website searches of the websites in the tabs. Each time the user taps `enter` in the chatbox, it should send the query to the websites. It won't send conversational queries like "Hi, how are you?" or terms it cannot recognize.

1. Experiment by adding or removing your QnA Maker knowledge base question and answers (in qnamaker.ai) and your LUIS intents/utterances (in luis.ai) and try new queries based on these changes. Each change in those sites must be trained and published before they will show up in the app.
