## Quick start

If you reading this - you probably wanted pagination, don't worry, we gotchu!

First, install the package. (No sh*t, Sherlock)
```
npm i spud.js@dev
```
`current version is; 2.0.0 (dev)`
After it's done installing, import it to your project/file:
```js
const Spud = require('spud.js');
```
Easy as that.

A simple example of the pagination:
```js
const { ButtonPaginationBuilder } = require('spud.js');
const { Client, MessageEmbed } = require('discord.js')
const client = new Client({...});

client.on('messageCreate', (message) => {
  const page1 = new MessageEmbed().setDescription('This is page 1')
  const page2 = new MessageEmbed().setDescription('This is page 2')
  if (message.content === 'pagination') {
    const pagination = new ButtonPaginationBuilder(message)
      .setEmbeds(page1, page2)

    pagination.send()
  }
})
```
Message and Embeds are **required** on paginations, add an embed or set embeds using [`.addEmbeds(...)`](https://github.com/MrPotato30/spudjs-docs/blob/main/docs/package/ButtonPaginationBuilder.md#addembedsembeds) or [`.setEmbeds(...)`](https://github.com/MrPotato30/spudjs-docs/blob/main/docs/package/ButtonPaginationBuilder.md#setembedsembeds)

---

Of course that is an example, but if you were to do something more advanced, let's add a 1 minute timer and enable fast skip for convenience
```js
const pagination = new ButtonPaginationBuilder(message)
  .setEmbeds(page1, page2)
  .setTimer(60000) // *optional (default 0)
  .fastSkip(true) // *optional (default false)

pagination.send()
```
Now our the pagination buttons will *automatically* be disabled after a minute, Pretty simple stuff right?

And thats it for the quickstart!
To explore all available features and options, feel free to look inside our [docs](https://github.com/MrPotato30/spudjs-docs/tree/main/docs) or visit our [website](https://spud.js.org)!

Please join our [support server](https://spudjs.repl.co/support)! Don't miss out next spud.js updates! 😉
