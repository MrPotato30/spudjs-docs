# <ins>MenuPaginationBuilder</ins>

## Constructor
```js
new MenuPaginationBuilder( data );
```
| PARAMETER   |      TYPE  | OPTIONAL   |
|----------|-------------|------|
| data |  [Message](https://discord.js.org/#/docs/discord.js/stable/class/Message) | |

## Methods

### .setOptions([...data]())
| PARAMETER   |      TYPE  |  OPTIONAL  |DESCRIPTION|
|----------|-------------|------|------|
| data |  [Object]() | | Set the select menu options the pagination instance uses | 

---

### .addOptions([...data]())
| PARAMETER   |      TYPE  |  OPTIONAL  |DESCRIPTION|
|----------|-------------|------|------|
| data |  [Object]() | | Add the select menu options the pagination instance uses | 

---
### .setHome([...embeds]())
| PARAMETER   |      TYPE  |  OPTIONAL  |DESCRIPTION|
|:---------:|:-------------:|:-----:|:-----:|
| embeds |  [MessageEmbed](https://discord.js.org/#/docs/discord.js/stable/class/MessageEmbed) |✅ |Embed before pagination is clicked | 
---

### setPlaceholder([activePlaceholder](), [ExpiredPlaceholder]())
| PARAMETER   |      TYPE  |  OPTIONAL  | DEFAULT |DESCRIPTION|
|:---------:|:-------------:|:---------:|:-------:|:---------:|
|     activePlaceholder      |       [String]()        |   ✅        |      " "   |      The placeholder when the select menu is active     |
|     expiredPlaceholder     |           [String]()    |    ✅       |        " " |      The placeholder when the select menu is expired    |
---

### setTime([ms]())
| PARAMETER   |  TYPE  |  OPTIONAL | DEFAULT |DESCRIPTION|
|:---------:|:-------------:|:-----:|:-----:|:-----:|
| ms | [Number]() | ✅ | 0 | Time until the pagination instance expires |
---

### setMax([max]())
| PARAMETER   |      TYPE  |  OPTIONAL | DEFAULT |DESCRIPTION|
|:---------:|:-------------:|:-----:|:-----:|:-----:|
| max | [Number]() | ✅ | 0 | Amount of clicks until pagination expires |
---

### setAuthor([user]())
| PARAMETER   |      TYPE  |  OPTIONAL  | DEFAULT |DESCRIPTION|
|:---------:|:-------------:|:-----:|:-----:|:-----:|
| user | [User](https://discord.js.org/#/docs/discord.js/stable/class/User) | ✅ | message.author / message.user | Author of the pagination instance |
---

### setChannel([channel]())
| PARAMETER   |      TYPE  |  OPTIONAL  | DEFAULT |DESCRIPTION|
|:---------:|:-------------:|:-----:|:-----:|:-----:|
| channel | [Channel](https://discord.js.org/#/docs/discord.js/stable/class/Channel) | ✅ | message.channel | Channel for the pagination instance |
---

### setContent([content]())
| PARAMETER   |      TYPE  |  OPTIONAL  | DEFAULT |DESCRIPTION|
|:---------:|:-------------:|:-----:|:-----:|:-----:|
| content | [String]() | ✅ | "" | Message content |
---

### replyOption([options](), [enabled]())
| PARAMETER   |      TYPE  |  OPTIONAL  | DEFAULT |DESCRIPTION|
|:---------:|:-------------:|:---------:|:-------:|:---------:|
| options | [Object]() | ✅ | { } | Reply to the message/interaction |
| enabled | [Boolean]() | ✅ | false | Reply options is enabled or not |
---

### setIdle([boolean]())
| PARAMETER   |      TYPE  |  OPTIONAL  | DEFAULT |DESCRIPTION|
|:---------:|:-------------:|:---------:|:-------:|:---------:|
|       boolean    |[Boolean]() |✅| false | Resets the timer on click|
---

### setFilter([User]())
| PARAMETER   |      TYPE  |  OPTIONAL  | DEFAULT |DESCRIPTION|
|:---------:|:-------------:|:---------:|:-------:|:---------:|
|    User|[User](https://discord.js.org/#/docs/discord.js/stable/class/User)   |✅          | message.author / message.user  |The user that can interact with the pagination|
---

### setComponents([components](), [event]())
| PARAMETER   |      TYPE  |  OPTIONAL |DESCRIPTION|
|:---------:|:-------------:|:---------:|:-------:|
|components|[Array]() / [MessageActionRow]()|   ✅  |       Allows for custom components to be added  |
|event|[function]() |   ✅      |       the event for the custom components  | 
---

### setInteraction([Boolean]())
| PARAMETER   |      TYPE  |  OPTIONAL  | DEFAULT |DESCRIPTION|
|:---------:|:-------------:|:---------:|:-------:|:---------:|
|      Boolean     |        [Boolean]()       |     ✅      |      false   |   enable interaction (for slash commands)        |
---
