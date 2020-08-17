+++
title = "Get Input from the command"
description = ""
weight = 1
+++

To get input from a command, we need to first structure our command in a certain way depending on the type of input.

### Getting a string or an int from a command

Lets say, we want to add a command that lets us set the name of the product. We have defined a function in `logic.js` named `onProductName`. This is how we should handle input.

#### `messages.js`

{{< code lang="js" >}}

	new Command({
        //`<your-input-name>` can be replaced with any sensible name
		command : "wg product name <your-input-name>",
        callback : logic.onProductName,
    });

{{< /code >}}



#### `logic.js`

{{< code lang="js" >}}

	module.exports.onProductName = () => {

        let inputValue = input['your-input-name'];

        //Rest of your code


    };

{{< /code >}}

The `logic.js` module has a local variable named `input` which stores any of the incoming input from the user. To understand how the variable `input` stores the input, please check [Bla bla](). The input value is mapped to a key defined earlier in the command string (`<your-input-name>`). 

### Sentence as an input

If the command requires a **more than one word** as an input. The user must use `""` between their input value. The example below shows how this works.

#### The command defined

{{< code lang="js" >}}
    wg product desc <description>
{{< /code >}}

#### Valid user message

{{< code lang="js" >}}
    wg product desc "Pudding can take over the world"
{{< /code >}}

#### Value in the input

{{< code lang="js" >}}
    input['description'] = "Pudding can take over the world";
{{< /code >}}

### Getting a media file as an input

To get images, files, and etc, we have to set the variable `requireMedia` in the Command constructor to `true`.

#### `messages.js`

{{< code lang="js" >}}
    new Command({
        command : "wg product image",
        callback : logic.onProductImage,
        requireMedia : true
    });
{{< /code >}}

#### `logic.js`

The input, which in this case a media file, is mapped to key `media`. Note that the value of the input is a [MessageMedia](https://pedroslopez.me/whatsapp-web.js/MessageMedia.html), which is a class defined in node package
['WhatsAppBot'](https://pedroslopez.me/whatsapp-web.js/).

{{< code lang="js" >}}
    module.exports.onProductImage = () => {
        let inputValue = input['media'];
        // rest of your code

    }
{{< /code >}}



