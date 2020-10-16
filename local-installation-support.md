# Local Installation Support

The bot can also be run locally without Heroku. The local setup requires more steps since the database needs to be setup and the development tools need be installed. Start with the steps 1 and 2 in [Setting up a New Bot](local-installation-support.md#new-bot) and the continue as follows:

## Step 1 - Create a local db <a id="step-1---create-a-local-db"></a>

Any Database that runs with SQL Sequelize \(‘https://sequelize.org/master/’\) can be used. My recommendation is to use the [SQL Lite](https://www.sqlite.org/index.html) database since the setup is fast and access is easy. Copy the connection details to the database for the next step. Example: The connection to a sqlite database with the name _database.db_ stored at the same level of this README file would be _./database.db_.

## Step 2 - Create a new .env File <a id="step-2---create-a-new-env-file"></a>

Copy the existing **.env.example** file and name it **.env**. Edit the Values of **DISCORD\_TOKEN**, **DISCORD\_BOT\_OWNER\_ID** and the **DATABASE\_URL** according to the values that you copied earlier.

## Step 3 - Install nodejs <a id="step-3---install-nodejs"></a>

Install nodejs from https://nodejs.org/en/

## Step 4 - Run and start the bot <a id="step-4---run-and-start-the-bot"></a>

Run `npm install -g gulp` in your console to install gulp. Build the bot code using `npm build` and run the bot with `npm start`.

## Step 5 - Configure Bot <a id="step-5---configure-bot"></a>

* Replace the CLIENTID string in the following URL with your own apps client id: https://discordapp.com/oauth2/authorize?&client\_id=CLIENTID&scope=bot&permissions=8
* Visit the resulting URL and add your bot to any server where you have admin privileges.
* Once added, your bot should show up more or less instantaneously. Type `!t help` within the discord chat for more details on how to use it. Happy translating!

