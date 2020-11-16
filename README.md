# Discord Timebomb

The "timebomb" command was a fun command found on several IRC bots that provided a light, entertaining form of amusement and user engagement. It worked a little like this:

* User A uses the "timebomb" command on User B.
* The IRC bot will ping User B and present them with a selection of coloured wires to cut, along with how much time is on the fuse.
* User B needs to respond back with the correct colour in order to defuse the bomb.
* If User B guesses the right colour, they are saved.
* If User B guesses the wrong colour, or if they don't respond by the time the timer runs out, the bomb will go off.

This is a recreation of the classic IRC timebomb command for [Discord](https://discord.com/), a popular web-based chat service. It is written for [blargbot](https://blargbot.xyz/), an open source Discord bot that can be added to any Discord server for free.

##Adding the bot to your server

You must be the Owner of, or have the Administrator permission on, the server you would like to add the command to. Then, you must add blargbot to your server, if the bot is not already on the server.

To add the bot to your server, do the following:

1. Go to the [blargbot website](https://blargbot.xyz/).
2. Select **MINVITE**.  
You may select **INVITE**; however, for best practices and security reasons, it is safer to use **MINVITE**.
3. Under **Add to Server**, select the name of the server you would like to add the bot to.
4. Select **Continue**.
5. Ensure that the following checkboxes are selected:  
  * Read Messages
  * Send Messages
  * Add Reactions
6. Select **Authorize**.
7. Go to Discord and select your server.  
The bot should have now joined the server and appear in the user list.
8. Select the server dropdown menu above the channel list and select **Server Settings**.  
The server settings menu opens.
9. Select **Roles**.
10. Select **blargbot** from the list.
11. Ensure that the **Read Message History** checkbox is selected.
12. Select the **X** icon, or press **Esc**, to close the settings menu.

The bot should now be in your server and have all of the necessary permissions to operate the command.

##Adding the command to your server

Once the bot has been added to your server, you may import the command to your server. There are two versions of the command you may import: the **Public Tags** version, and the **Custom Command** version.

The **Public Tags** version is easier to import, and will work out of the box without any additional setup. This is the recommended option for most users.

The **Custom Command** version requires more setup, but offers more customizability and flexibility than the Public Tags version.

###Adding the Public Tags version to your server

To add the Public Tags version of the command to your server, do the following:

1. Go to any channel on your server where the bot has access.  
You can see when the bot has access by entering `b!ping` in any text channel. If the bot responds, the bot has the needed permissions to read messages from and send messages to that channel.
2. Enter `b!cc import timebomb`.

The command will now be imported and available for use immediately.

###Adding the Custom Command version to your server

##Using the command

###Bombing a user

###Defusing a bomb

###Viewing the scores

Work in progress. See https://k6ka.blogspot.com/2020/05/timebomb-command-for-discord.html for details in the meantime.
