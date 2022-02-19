# MessagePagination
Represents an instance of pagination

## Constructor
```js
new MessagePagination({ options });
```
----
| Parameter         | Accepts           | Required |
| ----------------- | ----------------- | -------- |
| message           | [Message](https://discord.js.org/#/docs/discord.js/stable/class/Message)      | ✔️      |
| embeds            | Array             | ✔️      |
| buttons           | [buttonOptions]() |          |
| fastSkip          | Boolean           |          |
| time              | Number            |          |
| max               | Boolean           |          |
| author            | [User](https://discord.js.org/#/docs/discord.js/stable/class/User)             |          |
| channel           | [Channel](https://discord.js.org/#/docs/discord.js/stable/class/Channel)       |          |
| content           | String            |          |
| replyOptions      | [replyOptions]()  |          |
| resetTimerOnClick | Boolean           |          |
| pageTravel        | Boolean           |          |
----
### buttonOptions
Options required for creating custom buttons if you don't fancy the default ones.

**Types:**
- buttons: Array[object]
#### Usage
```js
const pagination = new MessagePagination({
  message,
  embeds: [embeds],
  buttons: [
    {
      name: 'first', // The button name you wish to modify
      emoji: '⬅️',
      style: 'SECONDARY', // Must be a valid discord button style,
    },
  ]
});
```

For checking what are valid buttons styles, check [here](https://discord.com/developers/docs/interactions/message-components#button-object-button-styles)

For buttons names that you can modify
### replyOptions
Options for replying to a specific message. Also allows you to disable pinging.

**Types:**
- message: [Message](https://discord.js.org/#/docs/discord.js/stable/class/Message)
- mention: Boolean
#### Usage
```js
const pagination = new MessagePaginaton({
  message,
  embeds: [embeds]
  replyOptions: {
    message: message // The message you wish to reply to
    mention: true // Set to false in order to not ping
  }
})
```
