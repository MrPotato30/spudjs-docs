# MenuPagination.options
### How to use "[.setOptions()](https://github.com/MrPotato30/spudjs-docs/tree/main/docs/packages/MenuPaginationBuilder#setoptionsdata)" and "[.addOptions()](https://github.com/MrPotato30/spudjs-docs/tree/main/docs/packages/MenuPaginationBuilder#addoptionsdata)"

---

## .setOptions([...Array]())
- Each array must include an Object with `label` and `embed`
- `embed` in every Array must be a valid Discord message embed
- Array size defines how many pages/options there are for the pagination

#### Example:
```js
let embed =  new Discord.MessageEmbed()
  .setTitle("this is page 1")

new MenuPaginationBuilder(message)
  .setOptions({
    label: "Page 1", // required
    embed // required (embed: embed)
  })
  .send() // send the pagination
```

#### Output: 
![Output](https://media.discordapp.net/attachments/825656508464758809/989852713879736350/unknown.png)

---

## .addOptions([...Array]())
- Push `Array` in MenuPagination.options
- Array size defines how many pages/options **added** for the pagination

#### Example:
```js
let embed =  new Discord.MessageEmbed()
  .setTitle("this is page 1")
  
let embed2 = new Discord.MessageEmbed()
  .setTitle("this is page 2")
  
let embed3 = new Discord.MessageEmbed()
  .setTitle("this is page 3")

new MenuPaginationBuilder(message)
  .setOptions(
    {label: "Page 1", embed},
    {label: "Page 2", embed: embed2}
  )
  .addOptions({label: "Page 3", embed: embed3})
  .send() // send the pagination
```

#### Output: 
![Output](https://media.discordapp.net/attachments/825656508464758809/989856103263252490/unknown.png)
