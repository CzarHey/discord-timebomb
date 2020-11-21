# Discord Timebomb

The "timebomb" command was a fun command found on several IRC bots that provided a light, entertaining form of amusement and user engagement. It worked a little like this:

* User A uses the "timebomb" command on User B.
* The IRC bot will ping User B and present them with a selection of coloured wires to cut, along with how much time is on the fuse.
* User B needs to respond back with the correct colour in order to defuse the bomb.
* If User B guesses the right colour, they are saved.
* If User B guesses the wrong colour, or if they don't respond by the time the timer runs out, the bomb will go off.

This is a recreation of the classic IRC timebomb command for [Discord](https://discord.com/), a popular web-based chat service. It is written for [blargbot](https://blargbot.xyz/), an open source Discord bot that can be added to any Discord server for free.

## Adding the bot to your server

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
The bot should have joined the server and appear in the user list.
8. Select the server dropdown menu above the channel list and select **Server Settings**.  
The server settings menu opens.
9. Select **Roles**.
10. Select **blargbot** from the list.
11. Ensure that the **Read Message History** checkbox is selected.
12. Select the **X** icon, or press **Esc**, to close the settings menu.

The bot should now be in your server and have all of the necessary permissions to operate the command.

## Adding the command to your server

Once the bot has been added to your server, you may import the command to your server. There are two versions of the command you may import: the **Public Tags** version, and the **Custom Command** version.

The **Public Tags** version is easier to import, and will work out of the box without any additional setup. This is the recommended option for most users.

The **Custom Command** version requires more setup, but offers more customizability and flexibility than the Public Tags version.

### Adding the Public Tags version to your server

To add the Public Tags version of the command to your server, do the following:

1. Go to any channel on your server where the bot has access.  
You can see when the bot has access by entering `b!ping` in any text channel. If the bot responds, the bot has the needed permissions to read messages from and send messages to that channel.
2. Enter `b!cc import timebomb`.

The command will now be imported and available for use immediately.

### Adding the Custom Command version to your server

The Custom Command version must be manually imported to your server and requires more setup, but allows for more flexibility and customization. It is recommended that you be familiar with Blargbot's functions before attempting to set up the Custom Command version.

To set up the Custom Command version of the command, do the following:

1. Go to the [BBTag Editor](https://blargbot.xyz/tags/editor).  
If you are prompted to allow the tool access to your account, select **Authorize**.
2. Under **Destination**, select the server you would like to add the command to from the dropdown menu.
3. Under **Tag Name**, enter the name you would like to use for the timebomb command. Users on your server will use this name to invoke the command. If you are not sure what to enter, enter `bomb` or `timebomb`.
4. Go to -insert link here-
5. Copy the code from the page and paste it in the BBTag Editor.
6. Select **Save**.  
The command will be created on your server.
7. Under **Tag Name**, enter `timebomb-channelbanlist`.
8. Select all of the text in the BBTag Editor and remove it.
8. Go to -insert link here-
9. Copy the code from the page and paste it in the BBTag Editor.
10. Select **Save**.  
The channel ban list will be created.
11. Under **Tag Name**, enter `timebomb-userbanlist`.
12. Select all of the text in the BBTag Editor and remove it.
13. Go to -insert link here-
14. Copy the code from the page and paste it in the BBTag Editor.
15. Select **Save**.  
The user ban list will be created.

## Using the command

Once added to your server, the command will work immediately, with no additional configuration needed.

### Bombing a user

To bomb a user, type `b!timebomb <user>`, replacing `<user>` with either:

* a username (e.g. `John#0101`)
* a user mention (e.g. `@John`)
* a user ID (you can obtain the ID number for a user after enabling [developer mode](https://support.discord.com/hc/en-us/articles/206346498-Where-can-I-find-my-User-Server-Message-ID-)

If multiple users have the same username, the bot may present you with a list of all matching usernames, prefixed with a number, as shown.

`<insert image here>`

When prompted, simply type the number of the user you wish to bomb. In the preceding example, to bomb `k6ka#1014`, type `1` in the channel. To cancel the query, type `c`.

### Defusing a bomb

When you are bombed, the bot will mention your username so you are notified. It will then provide you with a message containing three emoji reactions, consisting of a red, white, and blue circle, each representing a wire of the bomb.

**Accessibility note:** The red, white, and blue circles will *always* be presented in the same order.

To defuse the bomb, you need to cut one of the three wires shown. You do this by selecting one of the three emoji reactions below the bot's message.

`<insert image here>`

One of the three colours is designated as the correct wire colour. If you guess the right colour and select it, the bomb will be defused. If you guess the wrong colour, the bomb will detonate.

By default, bombs have a one minute timer. If you do not pick a wire by the time the timer runs out, the bomb will detonate.

### Viewing scores

The bot keeps track of the number of times you've:

* successfully defused a bomb
* failed to defuse a bomb
* ran out of time to defuse a bomb
* bombed other users

If you successfully defuse multiple bombs in a row, the bot will also keep track of your streak, as well as your highest winning streak for defusing bombs.

#### Viewing user scores

To view a user's scores, type `b!timebomb -s <user>`, replacing `<user>` with either:

* a username (e.g. `John#0101`)
* a user mention (e.g. `@John`)
* a user ID (you can obtain the ID number for a user after enabling [developer mode](https://support.discord.com/hc/en-us/articles/206346498-Where-can-I-find-my-User-Server-Message-ID-)

If multiple users have the same username, the bot may present you with a list of all matching usernames, prefixed with a number, as shown.

`<insert image here>`

When prompted, simply type the number of the user you wish to view the scores for. In the preceding example, to view the scores for `k6ka#1014`, type `1` in the channel. To cancel the query, type `c`.

#### Viewing server and global scores

The bot keeps track of the total scores for all users in a server, as well as globally (across all of Discord).

To view the scores for a server and for all of Discord, type `b!timebomb -s`, without providing a username after the `-s`.

## Managing the command

Server admins have the ability to configure certain aspects of the command for debugging, troubleshooting, or testing purposes.

Please note that, for maximum customizability, you should use the Custom Command version of the command. The Public Tags version of the command is much more limited in customization.

### Banning users from the command

You can ban individual users from using the command. Users who are banned will receive an error message when they try to use the command.

If you are using the Public Tags version of the command, please contact k6ka#1014 if you need to ban a user from the command. You can reach him on Blargbot's support server.

If you are using the Custom Command version of the command, you can ban users yourself. Before doing this, you must copy the user ID of the user you would like to ban. You may find instructions on how to do so in this [support article](https://support.discord.com/hc/en-us/articles/206346498-Where-can-I-find-my-User-Server-Message-ID-).

Then, do the following:

1. Open the [BBTag Editor](https://blargbot.xyz/tags/editor).
2. Under **Tag Name**, enter `timebomb-userbanlist`.
3. Select **Load**.  
The user ban list will load. By default, it will look like this:  
```{//;
Format is:
	<user ID> <name of user in comments>; true
}{switch;{userid};
	userID;true;
	false
}
```
4. Replace `userID;true;` with `X;true;`, with `X` being the user ID of the user you would like to ban.  
To ban multiple users, add a new line under the first entry, and follow the same format.  
Do not remove `false` or the bracket on the last line.
5. When finished, select **Save**.

### Banning channels from the command

You can ban individual channels from using the command. When a user tries to use the command in a banned channel, they will receive an error message.

If you are using the Public Tags version of the command, please contact k6ka#1014 if you need to ban a channel from the command. You can reach him on Blargbot's support server.

If you are using the Custom Command version of the command, you can ban channels yourself. Before doing this, you must copy the channel ID of the channel you would like to ban. You may find instructions on how to do so in this [support article](https://support.discord.com/hc/en-us/articles/206346498-Where-can-I-find-my-User-Server-Message-ID-).

Then, do the following:

1. Open the [BBTag Editor](https://blargbot.xyz/tags/editor).
2. Under **Tag Name**, enter `timebomb-channelbanlist`.
3. Select **Load**.  
The channel ban list will load. By default, it will look like this:  
```{//;
Format is:
    <channel ID> <name of channel in comments>; true
}{switch;{channelid};{//;
    }channelID;true;
    false
}
```
4. Replace `channelID;true;` with `X;true;`, with `X` being the channel ID of the channel you would like to ban.  
To ban multiple channel, add a new line under the first entry, and follow the same format.  
Do not remove `false` or the bracket on the last line.
5. When finished, select **Save**.

### Resetting a user's cooldown timer

When a user bombs another user for the first time, the bot will record the timestamp of when they used the command and saves it to its internal database. When the user bombs again, it will check for the timestamp. If it has been more than 60 seconds since the time on the timestamp, or if it cannot find the timestamp, the user will be allowed to bomb, and the bot will save a new timestamp. If it has been less than 60 seconds, the bot will not allow the user to bomb and will inform the user how much time they have to wait before being allowed to bomb again.

You can reset a user's cooldown timer by removing the timestamp. When the user attempts to bomb, the bot will not find a timestamp, and thus allow them to bomb again. This is useful for debugging and testing purposes where it would be inconvenient to wait one minute between bombings.

To reset a user's cooldown timer, do the following:

1. Enable [developer mode](https://support.discord.com/hc/en-us/articles/206346498-Where-can-I-find-my-User-Server-Message-ID-).
2. Right-click on the username of the user you would like to reset the cooldown timer for.
3. Select **Copy ID**.  
The user's user ID will be copied to your clipboard.
4. In any channel that the bot has access to, type `b!timebomb -r <user ID>`, replacing `<user ID>` with the user ID you copied in Step 3.

### Resetting a user's scores

You can reset the scores of a user, if needed. Note that this will only apply to the server you run the command on, and will not affect their scores in other servers. Resetting a user's scores does not affect the server or global scoreboard.

To reset a user's scores, do the following:

1. Enable [developer mode](https://support.discord.com/hc/en-us/articles/206346498-Where-can-I-find-my-User-Server-Message-ID-).
2. Right-click on the username of the user you would like to reset the scores for.
3. Select **Copy ID**.  
The user's user ID will be copied to your clipboard.
4. In any channel that the bot has access to, type `b!timebomb -t <user ID>`, replacing `<user ID>` with the user ID you copied in Step 3.

### Resetting a server's scores

You can reset a server's scoreboard. Note that this will only apply to the server you run the command on, and will not affect the scores in other servers. Resetting a user's scores does not affect the global scoreboard, nor will it reset the individual scores for each user.

To reset a server's scores, do the following:

1. In any channel that the bot has access to, type `b!timebomb -g`.  
To avoid accidental use, you will be asked to enter a confirmation message.
2. Enter the text that the bot asks you to retype exactly.  
Entering any other text or waiting 15 seconds will cancel the query.

### Changing the bomb timer

The bomb timer is the amount of time that users have to defuse the bomb before it goes off. By default, this is 60 seconds, or one minute.

If you are using the Public Tags version of the command, the bomb timer currently cannot be changed. If you are using the Custom Command version of the command, you can adjust the bomb timer by editing the code of the command. **Note that this is an advanced procedure and should not be attempted if you are not familiar with BBTag.**

To change the bomb timer, do the following:

1. Open the [BBTag Editor](https://blargbot.xyz/tags/editor) and load your timebomb command.
2. Under **Tag Name**, enter the name of your timebomb command that you had previously configured.
3. Select **Load**.
4. Press **Ctrl**-**F** (Windows) or **Command**-**F** (macOS).  
Your browser's find toolbar will open.
5. Enter `;60`.  
Your browser will locate all instances in the code that configure the bomb timer.
6. Replace `60` with the new time you would like to use, in seconds.
7. Change the output text in the command as needed to reflect the new change.

## Troubleshooting

### I am not seeing emoji reactions on the bot's messages

⚙

### Bot is throwing `No message found` errors

### Bot is throwing `This command was not authorized by server staff` errors

### Bot is throwing `I dont have permission to Add Reactions` errors

### Bot is not responding to bombed user's input

### Bomb does not go off after timer expires

### Command takes a very long time to execute before throwing an `An internal server error has occurred` error

Work in progress. See https://k6ka.blogspot.com/2020/05/timebomb-command-for-discord.html for details in the meantime.
