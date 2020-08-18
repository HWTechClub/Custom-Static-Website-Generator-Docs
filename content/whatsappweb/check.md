+++
title = "Check"
description = ""
weight = 8
+++

This function allows developers to avoid using repetitive if and else statement for basic checks. For example, checking if a website is selected before editing changes on the site. The check function requires two parameters in an object. 

* `checkFunction` - function that does a check on a specific subject and returns either an empty string or an array of string. An array of string indicates that the check has failed and the array of string must be send to the user. An empty string indicates indicates the check has passed and it must proceed to execute the `callback` function.
* `callback` - returns an array of string which is to be sent to the user.

## Example

#### `check()`

{{< code lang="js" >}}

    check({
        checkFunction : checkSelectedWebsiteExist(),
        Callback : () => {
            //Rest of your code, if the website exists 
        }
    });

{{< /code >}}

This function returns an array of string for the bot to send to the user. In this example, `check()` checks if the website exists by using the `checkSelectedWebsiteExist()`. `checkSelectedWebsiteExist()` return either an array of string or an empty string. If `checkSelectedWebsiteExist()` returns an array of string, then it would mean that there is no website and the array of string is send to the user. If `checkSelectedWebsiteExist()` returns an empty string, then the check would proceed to execute the callback function.

#### `checkSelectedWebsiteExist()`

{{< code lang="js" >}}

    const checkSelectedWebsiteExist= () => {

    if(user.getSelectedWebsite() == null)
    {
        return [
            `A website should be selected or created `,
            `To create website, please use the following command : `,
            `*wg create <company-name>*`,
        ];
    }

    return '';
}

{{< /code >}}

