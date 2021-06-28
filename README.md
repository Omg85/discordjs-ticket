# discordjs-ticket
## A simple discord ticket like ticket-tool
## Install
### NPM
```
$ npm install discordjs-ticket
```
### Yarn
```
$ yarn add discordjs-ticket
```
## Example 1
```js
const Ticket = require("discordjs-ticket").default; //require
client.ticket = new Ticket();
// ...
ticket.setTicketChannel(message.guild.channels.cache.get('CHANNEL_ID'), {
    title: "Ticket", //Title of the ticket
    description: "react here", //Description of ticket
    emoji: "❤️(option)", //Emoji you want 
    color: "GREEN(option)", //Color of the embed
});
// ...
client.ticket.on("create", (channel, user) => {
    console.log("Ticket Created!");
});
```

# Example 2
```js
client.on('message', async message => {
     if (message.content.startsWith("!set")) {
         ticket.setTicketChannel(message.guild.channels.cache.get('CHANNEL-ID'), {
             title: "asdf",
             description: "asdf",
             emoji: "❤️"
         });
     } else {
        
     }
});

client.ticket.on('create', (channel, user) => {
     console.log(channel, user);
 });
 ```

 # Other

 ```js
 .setTicketChannel //set ticket channel
 .createTicketChannel //create a ticket-channel
 //ticketChannel.send
 .closeTicket //close a ticket
