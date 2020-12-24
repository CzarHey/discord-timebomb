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
The bot should have joined the server and appeared in the user list.
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

The Custom Command version must be manually imported to your server and requires more setup, but allows for more flexibility and customization. It is recommended that you be familiar with blargbot's functions before attempting to set up the Custom Command version.

To set up the Custom Command version of the command, do the following:

1. Go to the [BBTag Editor](https://blargbot.xyz/tags/editor).  
If you are prompted to allow the tool access to your account, select **Authorize**.
2. Under **Destination**, select the server you would like to add the command to from the dropdown menu.
3. Under **Tag Name**, enter the name you would like to use for the timebomb command. Users on your server will use this name to invoke the command. If you are not sure what to enter, enter `bomb` or `timebomb`.
4. Go to https://github.com/CzarHey/discord-timebomb/blob/main/Custom%20Command/Timebomb%20(CC)
5. Copy the code from the page and paste it in the BBTag Editor.
6. Select **Save**.  
The command will be created on your server.
7. Under **Tag Name**, enter `timebomb-channelbanlist`.
8. Select all of the text in the BBTag Editor and remove it.
8. Go to https://github.com/CzarHey/discord-timebomb/blob/main/Custom%20Command/timebomb-channelbanlist
9. Copy the code from the page and paste it in the BBTag Editor.
10. Select **Save**.  
The channel ban list will be created.
11. Under **Tag Name**, enter `timebomb-userbanlist`.
12. Select all of the text in the BBTag Editor and remove it.
13. Go to https://github.com/CzarHey/discord-timebomb/blob/main/Custom%20Command/timebomb-userbanlist
14. Copy the code from the page and paste it in the BBTag Editor.
15. Select **Save**.  
The user ban list will be created.

The command will now be imported and can be used on your server.

## Using the command

Once added to your server, the command will work immediately, with no additional configuration needed.

### Bombing a user

To bomb a user, type `b!timebomb <user>`, replacing `<user>` with either:

* a username (e.g. `John#0101`)
* a user mention (e.g. `@John`)
* a user ID (you can obtain the ID number for a user after enabling [developer mode](https://support.discord.com/hc/en-us/articles/206346498-Where-can-I-find-my-User-Server-Message-ID-))

If multiple users have the same username, the bot may present you with a list of all matching usernames, prefixed with a number, as shown.

![Image of blarbot's multi-user selection panel](https://raw.githubusercontent.com/CzarHey/discord-timebomb/main/resources/blargbot%20multi-user%20selection%20demonstration.png)

When prompted, simply type the number of the user you wish to bomb. In the preceding example, to bomb `k6ka#1014`, type `1` in the channel. To cancel the query, type `c`.

### Defusing a bomb

When you are bombed, the bot will mention your username so you are notified. It will then provide you with a message containing three emoji reactions, consisting of a red, white, and blue circle, each representing a wire of the bomb.

**Accessibility note:** The red, white, and blue circles will *always* be presented in the same order.

To defuse the bomb, you need to cut one of the three wires shown. You do this by selecting one of the three emoji reactions below the bot's message.

![Image of the three emoji reactions that blargbot appends on the bombing message](https://raw.githubusercontent.com/CzarHey/discord-timebomb/main/resources/bomb%20wire%20colour%20emoji%20location.png)

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

![Image of blarbot's multi-user selection panel](https://raw.githubusercontent.com/CzarHey/discord-timebomb/main/resources/blargbot%20multi-user%20selection%20demonstration.png)

When prompted, simply type the number of the user you wish to view the scores for. In the preceding example, to view the scores for `k6ka#1014`, type `1` in the channel. To cancel the query, type `c`.

#### Viewing server and global scores

The bot keeps track of the total scores for all users in a server, as well as globally (across all of Discord).

To view the scores for a server and for all of Discord, type `b!timebomb -s`, without providing a username after the `-s`.

## Managing the command

Server admins have the ability to configure certain aspects of the command for debugging, troubleshooting, or testing purposes.

Please note that, for maximum customizability, you should use the Custom Command version of the command. The Public Tags version of the command is much more limited in customization.

### Banning users from the command

You can ban individual users from using the command. Users who are banned will receive an error message when they try to use the command.

If you are using the Public Tags version of the command, please contact k6ka#1014 if you need to ban a user from the command. You can reach him on blargbot's [support server](https://discord.gg/015GVxZxI8rtlJgXF).

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

If you are using the Public Tags version of the command, please contact k6ka#1014 if you need to ban a channel from the command. You can reach him on blargbot's [support server](https://discord.gg/015GVxZxI8rtlJgXF).

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

You can reset a user's cooldown timer by removing the timestamp. When the user attempts to bomb, the bot will not find a timestamp, and thus allows them to bomb again. This is useful for debugging and testing purposes where it would be inconvenient to wait one minute between bombings.

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

If you are not seeing emoji reactions under messages, you may have emoji reactions disabled. To enable them, do the following:

1. Go to **User Settings**. This is accessed by selecting the gear (⚙) icon at the bottom-left of the screen.
2. Select **Text & Images**.
3. Select **Show emoji reactions on messages**.  
The option will have a checkmark and be coloured green.
4. Select the **X** icon, or press **Esc**, to close the settings menu.

### Bot is throwing `No message found` errors

If you are seeing this error, the bot does not have access to view the message history of the current channel. To enable access to message history, do the following:

1. Select the server dropdown menu above the channel list and select **Server Settings**.  
The server settings menu opens.
2. Select **Roles**.
3. Select **blargbot** from the list.
4. Ensure that the **Read Message History** checkbox is selected.
5. Select the **X** icon, or press **Esc**, to close the settings menu.

### Bot is throwing `This command was not authorized by server staff` errors

If you are seeing this error, either the command was imported by someone who is not considered to be server staff by the bot, or the user who imported the command is no longer staff. The bot considers a user to be server staff if they have [these permissions](<https://discordapi.com/permissions.html#8254>).

If you are using the Public Tags version of the command, first find a user who is considered to be server staff by the bot, or ask the server owner to give you the needed permissions. Then, do the following:

1. Enter `b!cc delete timebomb`.  
The command will be removed from your server.
2. Enter `b!cc import timebomb`.  
The command will be reimported under the credentials of the user who imported it.

Deleting and reimporting the command will not affect the timebomb scores.

If you are using the Custom Command version of the command, follow Step 1 listed above to delete the command. Then, reimport the command using the instructions under **Adding the Custom Command version to your server** on this page. 

### Bot is throwing `I dont have permission to Add Reactions` errors

If you are seeing this error, the bot does not have access to add emoji reactions to messages. To grant access, do the following:

1. Select the server dropdown menu above the channel list and select **Server Settings**.  
The server settings menu opens.
2. Select **Roles**.
3. Select **blargbot** from the list.
4. Ensure that the **Add Reactions** checkbox is selected.
5. Select the **X** icon, or press **Esc**, to close the settings menu.

### Bot is not responding to bombed user's input

If the bot is not responding to the bombed user's input, this can be caused by one of two things:

* If the user selects an emoji reaction while the bot is still setting them up, that input will be ignored. Ask the user to remove their emoji reaction and try again.
* If the bot is lagged, it may miss user input. Ask the user to remove their emoji reaction and try again.
* If the bot goes down after the bomb is set, it will not be able to respond to user input. See the **Bomb does not go off after timer expires** section for additional details.

### Bomb does not go off after timer expires

If a bomb has been set but does not appear to go off even after the timer has supposedly expired, it is possible that the bot had gone down after the bomb was set. In this case, the bomb is effectively "cancelled"; the bot will not respond to user input, and no scores will be recorded.

### Command takes a very long time to execute before throwing an `An internal server error has occurred` error

If this occurs, the bot's database may be experiencing a temporary issue that prevents the cooldown timer from functioning correctly. Report the issue on the bot's support server.

## Known issues

### Scores get reset on the Custom Command version of the command when it is renamed

The Custom Command version uses local variables to store the scores. This is to prevent users with the right technical knowledge from changing the scores. It also prevents the scores from being lost if the command needs to be reauthorized under another user.

The consequence to this approach is that the scores are stored under the name that you initially created the command under. If you rename the command, the variables will not be moved over to the new name, and thus all scores will appear to have been reset. Reverting the rename and moving the command back to the old name will restore the scores.

This issues does not affect the Public Tags version of the command, as all scores are stored as author variables under k6ka's name. This ensures that they are consistent across servers and cannot be improperly manipulated by a bad actor.

### Mentions show `@invalid-user` on mobile after the bomb is detonated or defused

It is not entirely clear what exactly causes this issue. The issue is not present on the desktop app or on the browser version of Discord, nor does it affect mentions in the embed.

## Support

If you need help with the command, please join blargbot's [support server](https://discord.gg/015GVxZxI8rtlJgXF). My username is `k6ka#1014`; feel free to ping me and ask your question. If you share another server with me, you can also ping me there as well.

Please do not send me a friend request, as I do not accept friend requests from people I do not recognize.

## Changelog

* Version 1.0 (released May 8, 2020)
*  Initial release
* Version 1.1 (released June 21, 2020)
  * Switch "wireColor" and "wireColorText" to use temporary variables for faster performance.
  * Adjust bomb-failmsg mention positioning for consistency.
  * Add version and author information in command code.
* Version 1.1T (released July 26, 2020)
  * Initial release of the public tags import version.
* Version 1.2 (released July 30, 2020)
  * Restructure code for easier readability.
  * Update default message (used when no parameters are given) to use Discord embed.
  * Display version number in default message.
  * (Public tags version only) Default message displays creator name and CC BY-SA license.
  * Bot DMs the correct wire colour to the initiating user.
* Version 1.3 (released August 7, 2020)
  * Add built-in cooldown timer that prevents users from bombing again if they had already successfully bombed someone less than a minute ago.
  * Default message displays creator name and CC BY-SA license on both versions.
  * Add debug output flag for debugging purposes.
  * Add reset variables flag for debugging purposes.
  * Add experimental help flag to display help output.
  * Add information on where to report bugs for the command.
* Version 1.4 (released September 10, 2020)
  * Command now only sends one message. When the user picks a wire colour (or fails to select one in time), the bot will now edit the first message sent, rather than sending a second message.
  * Update success, fail, and timeout messages to reflect this new change.
  * Timeout messages broken off into separate auxiliary command.
  * Built-in cooldown timer uses local variables to address an exploit that allowed non-admins to reset their cooldown timer.
  * Update "user not found" message to include user mentions.
  * `currentTimeMinusLastTime` temporary variable no longer uses redundant `{userid}` tag.
  * Fix hidden `{waitreaction}` error (was only visible in debug output).
* Version 1.5 (released September 26, 2020)
  * Add scores feature that keeps track of user bombs, successful and unsuccessful defusals, timeouts, and win streaks.
  * Addressed an issue with the cooldown timer reset command that resulted in the rest of the command running erroneously when used.
  * Embed links show destination URL upon mouseover.
  * Remove redundant `{guildid}` subtag from local CC version.
* Version 2.0 (released December 23, 2020)
  * New features
    * Bomb messages are now formatted using Discord embeds.
    * Bomb messages show the user that threw the bomb to prevent "incognito" bombing.
    * New server and global scores feature added. Server scores keep track of the total scores on the current server, while global scores keep track of the total scores used on the command on all servers. Global scores are only available on the public tags version of the command.
    * New highest winning streak feature added. These keep track of the highest winning streak on a user, server, and global level.
    * Scores output now show the user avatar and server icon, if set.
    * Individual users, channels, and servers can now be banned from using the command.
    * Scores output is now available in the Public Tags version of the command.
    * Command now contains more descriptive built-in documentation.
  * Issues resolved
    * When there are multiple users with the same username, the bot will now provide a dialog allowing the user to choose the specified user from a list, rather than throwing a "User not found" error.
    * Users can no longer bomb users that are not on the current server by providing a user ID.
    * Command will now show a warning if the author of the command is not staff, rather than attempting to run the command without the needed permissions.
  * Behind-the-scenes changes
    * Debug output now exported to an external source due to its size. They are linked to from the command, and will expire seven days after being generated.
    * Success, fail, and timeout messages are now bundled with the command, meaning that auxiliary commands are no longer required for the command to work. All code is contained in the same command, making it much easier to import manually.
    * (Public tags version only) Scores now use author variables in order to allow them to persist across servers and remain the same even when the command is renamed locally. This will mean that any scores set prior to this update will be lost.
  * Other changes
    * This command's code is now hosted on GitHub to make it easier to organize and update in the future.
    * The public tags version is now drastically different from the CC version. The main differences include:
      * Scores use local variables instead of author variables, so they are not tied to the user who imported the command. This means that scores will not be carried over if the command is renamed.
      * Scores are entirely local and is not tied to the scores on the public tags system. This means that global scores are not available.
