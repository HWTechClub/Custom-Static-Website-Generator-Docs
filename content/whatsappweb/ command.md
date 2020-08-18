+++
title = "Command Class"
description = ""
weight = 1
+++

This defines the type for the user commands. Every `Command` is string with a callback function associated with it. We have flag variables to check  whether the command requires input or media .


{{< panel title="Properties" style="primary" >}}

    {{< listItems command callback requireMedia requireInput >}}

{{< /panel >}}

{{< panel title="Methods" style="primary" >}}

    {{< listItems "equals(message)" "_requireInput()" "getInput(message)" "_getInputMessage(msgString)" "_getSplitMessage(msg)" "_getInputMedia(message)" >}}

{{< /panel >}}

### Properties
<hr>

{{< prop title="command" type="string" >}}

command to be typed to execute the callback function

{{< prop title="callback" type="string[]" >}}

This is the function to be executed when the command is typed by the user. It should return an array of string, so that the bot send those as messages to the user.

{{< prop title="requireMedia" type="boolean" >}}

Determines whether a media should be attached with the command. Default set to false.

{{< prop title="requireInput" type="boolean" >}}

Determins whether the command needs an input value from the user.

### Methods
<hr>

{{< prop title="equals(message)" type="boolean" >}}

Checks if the command is exactly equal to user message.

{{< prop title="_requireInput()" type="void" >}}

This determines if the command requires input if the command has <inputName> in the string then the command requires input. Note, this is a private function as indicated by '_' sign. Also note, javascript does not have options to create a private function.

{{< prop title="getInput(message)" type="object" >}}

Gets the input from the `message`. The `message` parameter is a type of [Message](https://pedroslopez.me/whatsapp-web.js/Message.html) that can provide us both the message string and media files. This is an async function because getting the image from message is an asynchronous procedure.

Returns an object with the input values mapped to the keys defined in `command`.

{{< prop title="_getInputMessage(msgString)" type="object" >}}

Returns an object with input values that are strings. Only used for message with strings as input value.

{{< prop title="_getSplitMessage(msg)" type="string[]" >}}

Returns a splitted message from `msg` string.

{{< prop title="_getInputMedia(message)" type="object" >}}

Returns an object with input value that is a type of `MessageMedia`. Only used for message with media.

