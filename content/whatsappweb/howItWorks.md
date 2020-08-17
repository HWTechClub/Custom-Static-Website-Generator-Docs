+++
title = "How does the bot work"
description = ""
weight = 4
+++
We are using a node package to get the data from the WhatsApp. The [WhatsApp Bot](https://pedroslopez.me/whatsapp-web.js/) allows us to get messages, images, files, and also send messages, images, files back to the user as well. 
### Starting the bot
The bot starts a web driver, a [chrome web driver](https://chromedriver.chromium.org/), opening the Whatsapp web application. During the first usage of the bot, the WhatsApp web requires the developer to scan the QR code. Note that, this needs to be done only once. The next time you start the bot, you won't have to scan the QR code again.
 
### How does bot validate a message
After receiving a message, it checks if the message starts with `wg`. If it does, then it checks if the message is equal to any of the commands defined in our app. Then it proceeds to execute functions corresponding to the command defined. During this process, the bot identifies if there is any input from the user in the command. 
 
#### Example: Setting the cost of a product
 
{{< code >}}
    wg product cost 25
{{< /code >}}
 
This command will set the cost of a selected product to 25. 
 
#### Example: Setting description of a product
 
{{< code >}}
    wg product desc "Pudding mixed black pepper and bitter gourd"
{{< /code >}}
 
This will set the description. Notice how you have to use "" in this command between the description value. This helps identify a sentence and store it as an input.
 
#### Example: Setting image of a product
 
{{< code >}}
    wg product image **with the image attached**
{{< /code >}}
 
The bot will receive the image attached with command as the caption and save it to the product.
 
### Sending message to the user
 
The functions corresponding to the comma always return an array of string. The bot then receives the array and sends it to the user in WhatsApp.




