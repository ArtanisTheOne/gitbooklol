# Troubleshooting

* You can set up debugging Webhooks using the following steps
  1. Create a new channel on your server to receive the Webhooks, let’s say `#Webhooks`.
  2. Go to Server Settings -&gt; Webhooks -&gt; Create Webhook. Select the `#Webhooks` channel, then copy the Webhook’s URL. It will look something like `https://discordapp.com/api/webhooks/012345678901234567/VCj9yOOtJF9VCm-BU2F9xrbnoWD5gBZZ-UU1mZHcxi5VLgr3bPb9NanRJM8YD9cpBisL`
  3. In the **Settings** tab of your Heroku app add the following Config Variables \(values extracted from your URL\):
     * **DISCORD\_DEBUG\_WEBHOOK\_ID** : 012345678901234567
     * **DISCORD\_DEBUG\_WEBHOOK\_TOKEN** : VCj9yOOtJF9VCm-BU2F9xrbnoWD5gBZZ-UU1mZHcxi5VLgr3bPb9NanRJM8YD9cpBisL
  4. Restart your app’s `worker node src/bot.js` dyno, and you will begin to receive debugging messages in your `#Webhooks` channel.
* If your bot in unresponsive, the first thing to check is Heroku. Log in and manually restart the `worker node src/bot.js` dyno.
* For further troubleshooting, it’s helpful to install the Heroku command line interface. Once installed you can login from a terminal with `heroku login` and check your apps logs with `heroku logs --tail -a`
* If you are unable to solve a problem yourself, report it with as much detail as possible in this repo’s issue tracker.

