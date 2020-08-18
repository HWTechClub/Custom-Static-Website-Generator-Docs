+++
title = "How to add Commands"
description = ""
weight = 7
+++
To add a command, we make changes in the `messages.js` and `logic.js`. Firstly, in the `messages.js` we have to add a new instance of `Command` class in the `commands` array. A `Command` instance requires an object as a parameter. The parameter object has three fields. 

##### Create the command under commands array.

{{< code lang="js" >}}

    new Command({
        command : 'hello-world',
        callback : logic.onHelloWorld(),
        requireMedia : false,
    });

{{< /code >}}

* `command` - This holds the command string.
* `callback` - This requires a callback function which is executed when the user types the `command`. The callback function returns an array of string, that is sent to the user by the WhatsApp bot. 
* `requireMedia` - This tells us if the command requires an attached media with it. For example, an image.


##### What is `logic`?
As you can see, the callback function is called from logic module in `logic.js` . The purpose of having the function in logic.js is purely for having a clean code structure. Therefore, it is recommended to create the callback function in `logic.js`.

