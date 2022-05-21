# ButtonPaginationBuilder

### Constructor
```js
new ButtonPaginationBuilder( data );
```
| PARAMETER   |      TYPE  | OPTIONAL   |
|----------|-------------|------|
| data |  [Message](https://discord.js.org/#/docs/discord.js/stable/class/Message) | |

## Methods

### .setEmbeds([...embeds]())
| PARAMETER   |      TYPE  |  OPTIONAL  |DESCRIPTION|
|----------|-------------|------|------|
| embeds |  [MessageEmbed](https://discord.js.org/#/docs/discord.js/stable/class/MessageEmbed) | | The embeds to set

---

### .addEmbeds([...embeds]())
| PARAMETER   |      TYPE  |  OPTIONAL  |DESCRIPTION|
|----------|-------------|------|------|
| embeds |  [MessageEmbed](https://discord.js.org/#/docs/discord.js/stable/class/MessageEmbed) | | The embeds to add |

---

### .fastSkip([fastSkipEnabled]())

| PARAMETER   |      TYPE  |  OPTIONAL | DEFAULT  |DESCRIPTION|
|---------|-------------|:-----:|:-----:|:-----:|
| fastSkipEnabled | [Boolean]() | ✅ | false | Enable/disable fastSkip |

---

### .setTime([ms]())

| PARAMETER   |  TYPE  |  OPTIONAL | DEFAULT |DESCRIPTION|
|:---------:|:-------------:|:-----:|:-----:|:-----:|
| ms | [Number]() | ✅ | 0 | The time until the pagination expired |

---

### .setMax([max]())

| PARAMETER   |      TYPE  |  OPTIONAL | DEFAULT |DESCRIPTION|
|:---------:|:-------------:|:-----:|:-----:|:-----:|
| max | [Number]() | ✅ | 0 | Amount of clicks untill pagination expires |
