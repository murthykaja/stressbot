# Azure Stress Calculator Survery Bot

Bot Framework v4 QnA Maker bot sample. This sample shows how to integrate Multiturn and Active learning in a QnA Maker bot with ASP.Net Core-2. Click [here][72] to know more about using follow-up prompts to create multiturn conversation. To know more about how to enable and use active learning, click [here][71].

The bot is a customized version of a bot which has been created using [Bot Framework](https://dev.botframework.com). We have also used the [QnA Maker Service](https://www.qnamaker.ai) which enables us to build, train and publish a simple question and answer bot based on structured documents

## Concepts
- Azure Bot service and code design
- Azure Blob Service and linking to bot for storage of user response
- The [QnA Maker Service][19] to build, train and publish a simple question and answer bot structured documents.
    *The Active Learning to generate suggestions for knowledge base.
    *Use the Multiturn experience for the knowledge base .

# Architecture
![image](https://user-images.githubusercontent.com/84783754/120978602-47e0ce80-c792-11eb-8415-26cde484156e.png)
![image](https://user-images.githubusercontent.com/84783754/120979101-dbb29a80-c792-11eb-9053-0d1f78021b1a.png)


# Technical Details
- Azure Bot services – For creation of the Chatbot
- QnA Maker Service- For creation of the questionnaire posted via Chatbot
- Azure blob Storage- For storing user response as a blob
- Survey – Either hosted via web or through Telegram app.
- Bot Framework Emulator 4.13.0
- ngrok 2.0


# Configure Cognitive Service Model
- Create a Knowledge Base in QnAMaker Portal.
- Import "smartLightFAQ.tsv" file, in QnAMaker Portal.
- Save and Train the model.
- Create Bot from Publish page.
- Test bot with Web Chat.
- Capture values of settings like"QnAAuthKey" from 
- "Configuration" page of created bot, in Azure Portal.
- Updated appsettings.json with values as needed.
- Use value of "QnAAuthKey" for setting "QnAEndpointKey".
- Capture KnowledgeBase Id, HostName and EndpointKey current published app 


# Use Multi-turn prompt
- Once your QnA Maker service is up and you have published the sample KB, try the following queries to trigger the Train API on the bot.
- Sample query: "won't turn on"
- You can notice a prompt, included as part of  answer to query.



## Testing the bot using Bot Framework Emulator

[Bot Framework Emulator](https://github.com/microsoft/botframework-emulator) is a desktop application that allows bot developers to test and debug their bots on localhost or running remotely through a tunnel.

- Install the Bot Framework Emulator version 4.9.0 or greater from [here](https://github.com/Microsoft/BotFramework-Emulator/releases)

### Connect to the bot using Bot Framework Emulator

- Launch Bot Framework Emulator
- File -> Open Bot
- Enter a Bot URL of `http://localhost:3999/api/messages`
- Give Microsoft ID and password from .env file

# QnA Maker service
We have used Qna maker srevice to form questions and design the flow of survey. Generally Qna maker is used to answer the questions from user. But here we have used qna maker multi turn concept to navigate though the questions on the survey and record answers. 

# Telegram Link to access the bot:

http://t.me/StressCalulatorBot

# Learing Sorces
- [Bot Framework Documentation][20]
- [Bot Basics][32]
- [QnA Maker Documentation][23]
- [Active learning Documentation][50]
- [Activity Processing][25]
- [Azure Bot Service Introduction][21]
- [Azure Bot Service Documentation][22]
- [Azure CLI][7]
- [QnA Maker CLI][24]
- [Azure Portal][10]
- [Restify][30]
- [dotenv][31]

[1]: https://dev.botframework.com
[4]: https://nodejs.org
[5]: https://github.com/microsoft/botframework-emulator
[6]: https://github.com/Microsoft/BotFramework-Emulator/releases
[7]: https://docs.microsoft.com/en-us/cli/azure/?view=azure-cli-latest
[8]: https://docs.microsoft.com/en-us/cli/azure/install-azure-cli?view=azure-cli-latest
[9]: https://github.com/Microsoft/botbuilder-tools/tree/master/packages/MSBot
[10]: https://portal.azure.com
[19]: https://www.qnamaker.ai
[20]: https://docs.botframework.com
[21]: https://docs.microsoft.com/en-us/azure/bot-service/bot-service-overview-introduction?view=azure-bot-service-4.0
[22]: https://docs.microsoft.com/en-us/azure/bot-service/?view=azure-bot-service-4.0
[23]: https://docs.microsoft.com/en-us/azure/cognitive-services/qnamaker/overview/overview
[24]: https://github.com/Microsoft/botbuilder-tools/tree/master/packages/QnAMaker
[25]: https://docs.microsoft.com/en-us/azure/bot-service/bot-builder-concept-activity-processing?view=azure-bot-service-4.0
[30]: https://www.npmjs.com/package/restify
[31]: https://www.npmjs.com/package/dotenv
[32]: https://docs.microsoft.com/en-us/azure/bot-service/bot-builder-basics?view=azure-bot-service-4.0
[40]: https://aka.ms/azuredeployment
[50]: https://docs.microsoft.com/en-us/azure/cognitive-services/qnamaker/how-to/improve-knowledge-base
[51]: https://docs.microsoft.com/en-us/azure/cognitive-services/qnamaker/how-to/multiturn-conversation

[41]: https://docs.microsoft.com/en-us/azure/bot-service/bot-builder-howto-qna?view=azure-bot-service-4.0&tabs=cs
[71]: https://docs.microsoft.com/en-us/azure/cognitive-services/qnamaker/how-to/improve-knowledge-base
[72]: https://docs.microsoft.com/en-us/azure/cognitive-services/qnamaker/how-to/multiturn-conversation
