This defines the type for the user commands. Every Command is string with a callback function associated with it. We have flag variables to check  whether the command requires input or media .
Functions: 
    • Constructor : Initiates the object with given command and given function as callback function.
    • Equals() : check if the command is exactly equal to user message or the command requires an input
    • requireInput() : determines if the command needs an input or not
    • getInput(): Trims out the input or the media from the user message as required by the command
    • getSpiltmessage () : The above getInput function uses this function to trim out the message from the input from the user message string
    • getInputMedia() : GetInput function uses this function to get the media from the user message.
