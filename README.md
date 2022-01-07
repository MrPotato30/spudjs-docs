# Spud.js
<a href="https://www.npmjs.com/package/spud.js"><img src="https://img.shields.io/npm/dt/spud.js?maxAge=3600" alt="NPM downloads" /></a>
[![npm](https://img.shields.io/npm/v/spud.js.svg)](https://www.npmjs.com/package/spud.js)
[![install size](https://packagephobia.com/badge?p=spud.js)](https://packagephobia.com/result?p=spud.js)

[![NPM](https://nodei.co/npm/spud.js.png?downloads=true&downloadRank=true&stars=true)](https://nodei.co/npm/spud.js/)

Some cool package for discord.js :)
## Installation:
```
npm install spud.js
```

## Features:
- [pagination](https://en.wikipedia.org/wiki/Pagination#:~:text=Pagination%2C%20also%20known%20as%20paging,electronic%20pages%20or%20printed%20pages.) - Easiest way to make discord.js button pagination

### Require it in your file:
```js
const { pagination } = require('spud.js');
```
### Starter Template:
```js
const { Client, MessageEmbed } = require('discord.js');

const client = new Client({
  intents: [
    'GUILDS',
    'GUILD_MESSAGES',
  ],
});

client.on('messageCreate', async (message) => {
  if(message.content == 'pagination') {
    const embed1 = new MessageEmbed().setTitle('1');
    const embed2 = new MessageEmbed().setTitle('2');

    const pagination = new MessagePagination({
      message,
      embeds: [embed1, embed2],
      replyOptions: {
        mention: true,
        message,
      },
      content: 'This is a message content!',
    });
  }
});
```
### Custom pagination buttons:
```js
new MessagePagination({
  message,
  embeds: [embed1, embed2],
  button: [
    {
      name: 'first', // The button name you wish to modify
      emoji: '⬅️',
      style: 'SECONDARY', // Must be a valid discord button style
    },
  ],
});
```
For discord button styles refer to the [discord.js docs](https://discord.js.org/#/docs/main/stable/typedef/MessageButtonStyle) or [Discord Dev](https://discord.com/developers/docs/interactions/message-components#button-object-button-styles)
#### Button options:
- [first]() - Goes to the first page `(If fastSkip is set to true)`
- [previous]() - Goes to the previous page
- [next]() - Goes to the next page
- [last]()  - Goes to the last page `(If fastSkip is set to true)`
- [pageTravel]() - Type in the page you want to travel

## Planned
- Reaction pagination
- More things coming soon...!

### Options
- message - [Message](https://discord.js.org/#/docs/main/stable/class/Message) `required`
- embeds - [Array](https://developer.mozilla.org/en-US/docs/Glossary/Array) `required`
- author - [User](https://discord.js.org/#/docs/main/stable/class/User)
- channel - [Channel](https://discord.js.org/#/docs/main/stable/class/Channel)
- fastSkip - [Boolean](https://developer.mozilla.org/en-US/docs/Glossary/Boolean)
- time - [Number](https://developer.mozilla.org/en-US/docs/Glossary/Number)
- resetTimerOnClick -  [Boolean](https://developer.mozilla.org/en-US/docs/Glossary/Boolean)
- pageTravel - [Boolean](https://developer.mozilla.org/en-US/docs/Glossary/Boolean)
- max - [Number](https://developer.mozilla.org/en-US/docs/Glossary/Number)
- customFilter - [User#id](https://discord.js.org/#/docs/main/stable/class/User?scrollTo=id)
- button - [Array](https://developer.mozilla.org/en-US/docs/Glossary/Array)
- messageReply - [Message](https://discord.js.org/#/docs/main/stable/class/Message)
- content - [String](https://developer.mozilla.org/en-US/docs/Glossary/String)
