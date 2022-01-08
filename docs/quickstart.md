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
