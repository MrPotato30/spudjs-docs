# <ins>ButtonPaginationBuilder</ins>

## Constructor
```js
new ButtonPaginationBuilder( data );
```
| PARAMETER   |      TYPE  | OPTIONAL   |
|----------|-------------|------|
| data |  [Message](https://discord.js.org/#/docs/discord.js/stable/class/Message) | |

## Methods

### .setEmbeds([...embeds]())[*]()
| PARAMETER   |      TYPE  |  OPTIONAL  |DESCRIPTION|
|----------|-------------|------|------|
| embeds |  [MessageEmbed](https://discord.js.org/#/docs/discord.js/stable/class/MessageEmbed) | | Embeds the pagination instance uses

---

### .addEmbeds([...embeds]())[*]()
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
| ms | [Number]() | ✅ | 0 | Time until the pagination instance expires |

---

### .setMax([max]())

| PARAMETER   |      TYPE  |  OPTIONAL | DEFAULT |DESCRIPTION|
|:---------:|:-------------:|:-----:|:-----:|:-----:|
| max | [Number]() | ✅ | 0 | Amount of clicks until pagination expires |


---

### .setAuthor([User]())

| PARAMETER   |      TYPE  |  OPTIONAL  | DEFAULT |DESCRIPTION|
|:---------:|:-------------:|:-----:|:-----:|:-----:|
| User | [User](https://discord.js.org/#/docs/discord.js/stable/class/User) | ✅ | message.author | Author of the pagination instance |

---

### .setChannel([Channel]())

| PARAMETER   |      TYPE  |  OPTIONAL  | DEFAULT |DESCRIPTION|
|:---------:|:-------------:|:-----:|:-----:|:-----:|
| Channel | [Channel](https://discord.js.org/#/docs/discord.js/stable/class/Channel) | ✅ | message.channel | Channel for the pagination instance |

---

### .setContent([content]())

| PARAMETER   |      TYPE  |  OPTIONAL  | DEFAULT |DESCRIPTION|
|:---------:|:-------------:|:-----:|:-----:|:-----:|
| content | [String]() | ✅ | "" | Message content |

---

### .replyOption([options](), [enabled]())

| PARAMETER   |      TYPE  |  OPTIONAL  | DEFAULT |DESCRIPTION|
|:---------:|:-------------:|:-----:|:-----:|:-----:|
| options | [Object]() | ✅ | { } | Reply to the message/interaction |
| enabled | [Boolean]() | ✅ | false | Reply options is enabled or not |

---
### .setIdle([idle]())

| PARAMETER   |      TYPE  |  OPTIONAL  | DEFAULT |DESCRIPTION|
|:---------:|:-------------:|:---------:|:-------:|:---------:|
|       idle    |[Boolean]() |✅| false | Resets the timer on click|

---

### .pageTravel([boolean]())

| PARAMETER   |      TYPE  |  OPTIONAL  | DEFAULT |DESCRIPTION|
|:---------:|:-------------:|:---------:|:-------:|:---------:|
|    boolean|[Boolean]()   |✅          |   false  |  Allows you use numbers for navigation  |

---

### .setComponents([components](), [event]())

| PARAMETER   |      TYPE  |  OPTIONAL |DESCRIPTION|
|:---------:|:-------------:|:---------:|:-------:|
|components|[Array]() / [MessageActionRow]()|   ✅  |       Allows for custom components to be added  |
|event|[function]() |   ✅      |       the event for the custom components  | 

---

### .trash([Boolean]())

| PARAMETER   |      TYPE  |  OPTIONAL  | DEFAULT |DESCRIPTION|
|:---------:|:-------------:|:---------:|:-------:|:---------:|
|    Boolean|[Boolean]()   |✅          |   false  |  Adds a button to delete the current pagination instance.  |

---

### .setButton([name](), [properties]())
- see [example](https://github.com/MrPotato30/spudjs-docs/blob/main/docs/packages/ButtonPaginationBuilder/ButtonData.md#example)
- ButtonNames: [Click here](https://github.com/MrPotato30/spudjs-docs/blob/main/docs/packages/ButtonPaginationBuilder/ButtonData.md#buttonnames)
- ButtonProperties: [Click here](https://github.com/MrPotato30/spudjs-docs/blob/main/docs/packages/ButtonPaginationBuilder/ButtonData.md#buttonproperties)

[Click here](https://github.com/MrPotato30/spudjs-docs/blob/main/docs/packages/ButtonPaginationBuilder/ButtonData.md) to learn how to use `.setButton`


| PARAMETER   |      TYPE  |  OPTIONAL  | DEFAULT |DESCRIPTION|
|:---------:|:-------------:|:---------:|:-------:|:---------:|
|    name| [String]() / [ButtonNames](https://github.com/MrPotato30/spudjs-docs/blob/main/docs/packages/ButtonPaginationBuilder/ButtonData.md#buttonnames)   |✅          |   " "  |  Name of the button you wish to customize  |
|    properties| [Object]() / [ButtonProperties](https://github.com/MrPotato30/spudjs-docs/blob/main/docs/packages/ButtonPaginationBuilder/ButtonData.md#buttonproperties)   |✅          |   { }  | Allows you to customize button properties  

---

### .setFilter([User]())

| PARAMETER   |      TYPE  |  OPTIONAL  | DEFAULT |DESCRIPTION|
|:---------:|:-------------:|:---------:|:-------:|:---------:|
|    User|[User](https://discord.js.org/#/docs/discord.js/stable/class/User)   |✅          |   |s a button to delete the current pagination instance.  |

---
