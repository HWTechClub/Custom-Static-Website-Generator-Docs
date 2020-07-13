+++
title = "Commands"
description = ""
weight = 2
+++
## Single template
At the current moment we only have one template which is a e-commerce template. Read commands refer to commands to get some information and send commands to send some
details.

##### 1. Read Command : !info
Returns the procedures to get started with the website
{{< code lang="js" >}}
// Code that sends the following messages back to whatsapp (i.e RESPONSE)

client.sendMessage(msg.from,`*We are still working userflow interactions and use this is the BETA release*. Currently we only accept image url's.`);
client.sendMessage(msg.from,"For entering details enter details using the following syntax :");
client.sendMessage(msg.from,"1. *Command* !details firstName,lastName,companyName,logoUrl,bannerUrl,email,description");
client.sendMessage(msg.from,"2. *Command* new row");
client.sendMessage(msg.from,"Please do wait for the commands to appear");
client.sendMessage(msg.from,"3. *Command* !done : Must be added after each row is added");
client.sendMessage(msg.from,"4. *Command* !finished : To ensure the deploy the website");
client.sendMessage(msg.from,"The current version we are using you can only use a single template and only generate new websites");

{{< /code >}}

##### 2. Send Command : !details
Sends basic information like owner details
{{< code lang="" >}}
//Request Parameters
!details <First Name>,<Last Name>,<Company Name>,<Company logo url>,<Banner url>,<Email>,<Description>

//No Response

{{< /code >}}

##### 3. Read Command : !new row
Returns commands to add more information (i.e product information)
{{< code lang="js" >}}
// Code that sends the following messages back to whatsapp (i.e RESPONSE)

msg.reply("Enter the following commands:");
client.sendMessage(msg.from, 'product id: *INFORMATION GOES HERE*');
client.sendMessage(msg.from, 'product name: *INFORMATION GOES HERE*')
client.sendMessage(msg.from, 'description: *INFORMATION GOES HERE*')
client.sendMessage(msg.from, 'cost: *INFORMATION GOES HERE*')
client.sendMessage(msg.from, 'product image: *ATTACH IMAGE HERE*')
client.sendMessage(msg.from, '!done when all information is entered')
{{< /code >}}

##### 4. Write Command : Product id , Product name , Description , Cost, Product Image 
