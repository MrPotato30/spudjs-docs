# How to customize your buttons
### Guide to customize your message embed pagination button (1.2.11)
- first, we are going to add `button` option to the message embed option
```js
new MessagePagination({
  message, // required
  embeds: [...], // required
  button: [...], // our button option
});
```

- then, we have to specify what button we want to modify;
```js
new MessagePagination({
  message, // required
  embeds: [...], // required
  button: [{name: "...", emoji: "...", style: "..."}], // our button option
});
```

### Options:
- [name](https://github.com/MrPotato30/spudjs-docs/new/main/docs/MessagePagination#button-names)
- emoji
- [style](https://discord.com/developers/docs/interactions/message-components#button-object-button-styles) `must be a valid discord.js button style`

## Example:
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

### Button names:
- first `Note: Only be displayed if fastSkip: true`
- previous
- next
- last `Note: Only be displayed if fastSkip: true`
- pageTravel `Note: Only be displayed if pageTravel: true`
