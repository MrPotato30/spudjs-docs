## Quick start

If you reading this - you probably wanted in pagination, don't worry, we gotchu!

First of all, install the package
```
npm i spud.js@latest
```
After it's installed import it:
```js
const { MessagePagination } = require('spud.js');
```

Then a basic bot example would be something like:
```js
const { MessagePagination } = require('spud.js');
const { Client, MessageEmbed } = require('discord.js')
const client = new Client({
  intents: [
     'GUILDS',
     'GUILD_MESSAGES'
  ],
});

client.on('messageCreate', (message) => {
  const page1 = new MessageEmbed().setTitle('1').setDescription('one')
  const page2 = new MessageEmbed.setTitle('2').setDescription('two')
  if (message.content === 'pagination') {
    const pagination = new MessagePagination({
      message,
      embeds: [page1, page2]
    })   
  }
})
```
Of course this is but an example but if you were to do something more advanced, lets say we disable pinging and reply to a message, we'll add a custom timer and choose fast skips for convenience
```js
const pagination = new MessagePagination({
  message,
  embeds: [page1, page2],
  fastSkip: true,
  replyOptions: {
    mention: false,
    message
  },
  time: 6000
})
```
Pretty simple stuff right?

And thats it for the quickstart!
To check all available options, look inside our [documentation!(coming soon)](https://github.com/MrPotato30/spudjs-docs)
