# ButtonPaginationBuilder

## Constructor
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


---

### .setAuthor([User]())

| PARAMETER   |      TYPE  |  OPTIONAL  | DEFAULT |DESCRIPTION|
|:---------:|:-------------:|:-----:|:-----:|:-----:|
| User | [User](https://discord.js.org/#/docs/discord.js/stable/class/User) | ✅ | message.author | the author of the pagination |

---

### .setChannel([Channel]())

| PARAMETER   |      TYPE  |  OPTIONAL  | DEFAULT |DESCRIPTION|
|:---------:|:-------------:|:-----:|:-----:|:-----:|
| Channel | [Channel](https://discord.js.org/#/docs/discord.js/stable/class/Channel) | ✅ | message.channel | the channel for pagination |

---

### .setContent([content]())

| PARAMETER   |      TYPE  |  OPTIONAL  | DEFAULT |DESCRIPTION|
|:---------:|:-------------:|:-----:|:-----:|:-----:|
| content | [String]() | ✅ | "" | message content |

---

### .replyOption([options](), [enabled]())

| PARAMETER   |      TYPE  |  OPTIONAL  | DEFAULT |DESCRIPTION|
|:---------:|:-------------:|:-----:|:-----:|:-----:|
| options | [Object]() | ✅ | { } | reply to the message/interaction |
| enabled | [Boolean]() | ✅ | false | reply options is enabled or not |

---

### .setIdle()
| PARAMETER   |      TYPE  |  OPTIONAL  | DEFAULT |DESCRIPTION|
|:---------:|:-------------:|:---------:|:-------:|:---------:|
|           |[Boolean]() |✅| 
|           |            |   |          |         |           |

---

## .pageTravel()
| PARAMETER   |      TYPE  |  OPTIONAL  | DEFAULT |DESCRIPTION|
|:---------:|:-------------:|:---------:|:-------:|:---------:|
|           |[Boolean]() |✅|           |         |          | 
|           |            |   |          |         |           |

---

## .setComponents()
| PARAMETER   |      TYPE  |  OPTIONAL  | DEFAULT |DESCRIPTION|
|:---------:|:-------------:|:---------:|:-------:|:---------:|
|           |[Events]() |✅|           |         |          | 
|           |[Components]()|✅|          |         |           |

