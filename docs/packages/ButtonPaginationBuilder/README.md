[User]: https://discord.com/developers/docs/resources/user
[Channel]: https://discord.com/developers/docs/resources/channel
[Message]: https://discord.js.org/#/docs/discord.js/stable/class/Message
[MessageActionRow]: https://discord.js.org/#/docs/discord.js/stable/class/MessageActionRow
[MessageEmbed]: https://discord.js.org/#/docs/discord.js/stable/class/MessageEmbed
[MessageComponents]: https://discord.com/developers/docs/interactions/message-components


# <ins>ButtonPaginationBuilder</ins>

## Constructor
```js
new ButtonPaginationBuilder( data );
```
| PARAMETER |   TYPE   | OPTIONAL |
|:---------:|:--------:|:--------:|
| data      |[Message]() |   ❎       |

## Methods

### .setEmbeds([...embeds]())[*]()
| PARAMETER |    TYPE     | OPTIONAL |       DESCRIPTION        |
|:---------:|:-----------:|:--------:|:-----------------------------------:|
| embeds |  [MessageEmbed]()|     ❎     | Embeds the pagination uses |

---

### .addEmbeds([...embeds]())[*]()
| PARAMETER   |      TYPE  |  OPTIONAL  |DESCRIPTION|
|:---------:|:-----------:|:--------:|:-----------------------------------:|
| embeds |  [MessageEmbed]()| ❎| The embeds to add |

---

### .fastSkip([fastSkipEnabled]())

| PARAMETER   |      TYPE  |  OPTIONAL | DEFAULT  |DESCRIPTION|
|---------|-------------|:-----:|:-----:|:-----:|
| fastSkipEnabled | [Boolean]() | ✅ | false | Enable/disable fastSkip |

---

### .setTime([ms]())

| PARAMETER   |  TYPE  |  OPTIONAL | DEFAULT |DESCRIPTION|
|:---------:|:-------------:|:-----:|:-----:|:-----:|
| ms | [Number]() | ✅ | 0 | Time until the pagination expires |

---

### .setMax([max]())

| PARAMETER   |      TYPE  |  OPTIONAL | DEFAULT |DESCRIPTION|
|:---------:|:-------------:|:-----:|:-----:|:-----:|
| max | [Number]() | ✅ | 0 | Amount of clicks until pagination expires |


---

### .setAuthor([User])

| PARAMETER   |      TYPE  |  OPTIONAL  | DEFAULT |DESCRIPTION|
|:---------:|:-------------:|:-----:|:-----:|:-----:|
| User | [User]| ✅ | message.author / message.user | Author of the pagination |

---

### .setChannel([Channel])

| PARAMETER   |      TYPE  |  OPTIONAL  | DEFAULT |DESCRIPTION|
|:---------:|:-------------:|:-----:|:-----:|:-----:|
| Channel | [Channel] | ✅ | message.channel | Channel for the pagination |

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
|components|[Array]() / [MessageActionRow]|✅|Allows for custom components to be added  |
|collect|[function]() |✅|The event for the custom components|
|end|[function]()|✅|The event when the collector ends|

---

### .trash([Boolean]())

| PARAMETER   |      TYPE  |  OPTIONAL  | DEFAULT |DESCRIPTION|
|:---------:|:-------------:|:---------:|:-------:|:---------:|
|    Boolean|[Boolean]()   |✅          |   false  |  Adds a button to delete the current pagination.  |
---
### .pageFooter([Boolean]())
| PARAMETER   |      TYPE  |  OPTIONAL  | DEFAULT |DESCRIPTION|
|:---------:|:-------------:|:---------:|:-------:|:---------:|
|toggle|[Boolean]()|✅|true|Toggle the pagination footer|
---

### .setButtons([name](), [properties]())
- see [example](https://github.com/MrPotato30/spudjs-docs/blob/main/docs/packages/ButtonPaginationBuilder/ButtonData.md#example)
- ButtonNames: [Click here](https://github.com/MrPotato30/spudjs-docs/blob/main/docs/packages/ButtonPaginationBuilder/ButtonData.md#buttonnames)
- ButtonProperties: [Click here](https://github.com/MrPotato30/spudjs-docs/blob/main/docs/packages/ButtonPaginationBuilder/ButtonData.md#buttonproperties)

[Click here](https://github.com/MrPotato30/spudjs-docs/blob/main/docs/packages/ButtonPaginationBuilder/ButtonData.md) to learn how to use `.setButton`


| PARAMETER   |      TYPE  |  OPTIONAL  | DEFAULT |DESCRIPTION|
|:---------:|:-------------:|:---------:|:-------:|:---------:|
|    name| [String]() / [ButtonNames](https://github.com/MrPotato30/spudjs-docs/blob/main/docs/packages/ButtonPaginationBuilder/ButtonData.md#buttonnames)   |✅          |   " "  |  Name of the button you wish to customize  |
|    properties| [Object]() / [ButtonProperties](https://github.com/MrPotato30/spudjs-docs/blob/main/docs/packages/ButtonPaginationBuilder/ButtonData.md#buttonproperties)   |✅          |   { }  | Allows you to customize button properties  

---

### .setFilter([User])

| PARAMETER   |      TYPE  |  OPTIONAL  | DEFAULT |DESCRIPTION|
|:---------:|:-------------:|:---------:|:-------:|:---------:|
|    User|[User]   |✅          | message.author / message.user  |The user that can interact with the pagination|
