# Spud.js Documentation
### Welcome to spud.js! Get started with spud.js npm package, very easy to use and user-friendly multipurpose npm package and api for <a href="https://discord.js.org/#/" target="_blank">discord.js v13</a>.
#### If you don't understand something in the documentation, you are experiencing problems, or you just need support, please don't hesitate to join our official <a href="https://discord.gg/7MaXqCy6JH">support server</a>.

### installing the package: <a href="https://www.npmjs.com/package/spud.js"><img src="https://img.shields.io/npm/v/spud.js?maxAge=3600" alt="NPM version" /></a>
###### installing the latest version of spud.js:
```js
npm install spud.js@latest
```

### Define the package:
```js
const spud = require('spud.js');
```

# Basics
#### Quick pagination:
```js
const embed1 = new MessageEmbed().setTitle('First Embed');
const embed2 = new MessageEmbed().setTitle('Second Embed');

const pagination = new MessagePagination({
  message,
  embeds: [embed1, embed2]
})
```

#### Custom Buttons:
```js
const embed1 = new MessageEmbed().setTitle('First Embed');
const embed2 = new MessageEmbed().setTitle('Second Embed');

const pagination = new MessagePagination({
  message,
  embeds: [embed1, embed2]
  button: [
    {
      name: 'first', // The button name you wish to modify
      emoji: '⬅️',
      style: 'SECONDARY', // Must be a valid discord button style
    },
  ],
})
```
For discord button styles refer to the [discord.js docs](https://discord.js.org/#/docs/main/stable/typedef/MessageButtonStyle) or [Discord Dev](https://discord.com/developers/docs/interactions/message-components#button-object-button-styles)
#### Button options:
- [first]() - Goes to the first page `(If fastSkip is set to true)`
- [previous]() - Goes to the previous page
- [next]() - Goes to the next page
- [last]()  - Goes to the last page `(If fastSkip is set to true)`
- [pageTravel]() - Type in the page you want to travel

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
- replyOptions - { message: [Message](https://discord.js.org/#/docs/main/stable/class/Message), mention: [Boolean](https://developer.mozilla.org/en-US/docs/Glossary/Boolean) }
- content - [String](https://developer.mozilla.org/en-US/docs/Glossary/String)

## All Options enabled:
```js
new MessagePagination({
  message: message,
  embeds: [],
  author: message.author,
  channel: message.channel,
  fastSkip: true,
  time: 60000 * 5, //5 minutes
  resetTimerOnClick: true,
  pageTravel: true,
  max: 10,
  customFilter: message.author.id,
  button: [],
  replyOptions: {message: message, mention: true},
  content: "Pagination by spud.js"
})
```
