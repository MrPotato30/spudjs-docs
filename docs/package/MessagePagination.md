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
| button            | [buttonOptions]() |          |
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
- button: Array[object]
#### Usage
```js
const pagination = new MessagePagination({
  message,
  embeds: [embeds],
  button: [
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

## Slash Commands
*inside replyOptions*
- interaction: \<Boolean> `must be set to **true**`
- type: \<String> |  available options: [followUp](https://discord.js.org/#/docs/discord.js/stable/class/BaseCommandInteraction?scrollTo=followUp) / [editReply](https://discord.js.org/#/docs/discord.js/stable/class/ButtonInteraction?scrollTo=editReply) / [reply](https://discord.js.org/#/docs/discord.js/stable/class/ButtonInteraction?scrollTo=reply) `default: "reply"`
### example:
```js
const pagination = new MessagePaginaton({
  message: interaction
  embeds: [embeds]
  replyOptions: {
    interaction: true,
    type: "followUp"
  }
})
```
