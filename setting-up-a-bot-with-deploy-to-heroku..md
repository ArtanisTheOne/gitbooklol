# Setting up a Bot with Deploy to Heroku.

Rita is a an automatic translation bot built using `discord.js` and `Google Translate API`.

This Method does not need you to Fork this repository, you can run your not straight off of the Rita Master Branch. For update instructions click [here](how-to-update-to-1.1.7-and-above.md)

## Deploy to Heroku. <a id="deploy-to-heroku"></a>

### Step 1 - Create a new [Discord App](https://discordapp.com/developers/applications/me/create) <a id="step-1---create-a-new-discord-app"></a>

* Give app a friendly name and click the **Create App** button
  * I like the name **C-3PO**, but feel free to pick something different if you fear George Lucas’s wrath. Maybe **C-4PO**
* Take note of the app **CLIENT ID**, you will need it later
* Scroll down to the **Bot** section
* Click the **Create a Bot User** button
* Click the **Yes, do it!** button
* Copy the bot’s **TOKEN**, you will need it later

### Step 2 - Deploy to Heroku <a id="step-2---deploy-to-heroku"></a>

[![Deploy to Heroku](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy?template=https://github.com/Zyc0r3/RitaBot)

* In the custom variable of **DISCORD\_TOKEN** put in the copied token of your created bot.
* **DO NOT CHANGE** the **NODE\_MODULES\_CACHE** Variable unless you know about Heroku Caching.
* If you with to use Webhook Debug logging:
  * Fill in **DISCORD\_DEBUG\_WEBHOOK\_ID** & **DISCORD\_DEBUG\_WEBHOOK\_TOKEN**, For instructions go [here](setting-up-a-bot-with-deploy-to-heroku..md#troubleshooting)
* Once installed, Go to the **Overview** tab and click configure dynos. Turn off the default `web npm start` dyno and turn on the `worker node src/bot.js` dyno. Your bot will now be up and running!

### Step 3 - Invite your bot to your server and configure it! <a id="step-3---invite-your-bot-to-your-server-and-configure-it"></a>

* Replace the CLIENTID string in the following URL with your own apps client id from Step 2: https://discordapp.com/oauth2/authorize?&client\_id=CLIENTID&scope=bot&permissions=8
* Visit the resulting URL and add your bot to any server where you have admin privileges.
* Once added, your bot should show up more or less instantaneously. Type `!t help` within the discord chat for more details on how to use it. Happy translating!

