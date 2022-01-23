# Base URL
```
https://welcomer.spudjs.repl.co/
```

### Options
- tag
- avatar
- text1
- text2
- background
---
#### Example
```js

const Discord = require('discord.js'),
const axios = require('axios')
const client = new Discord.Client({ options });

client.on('guildMemberAdd', async(member) => {
  const card = await axios.get(`welcomer.spudjs.repl.co/generate?tag=${member.user.tag}&avatar=${member.user.displayAvatarURL({format: 'png'})}&background=https://i.pinimg.com/originals/90/cd/dc/90cddc7eeddbac6b17b4e25674e9e971.jpg`)
  const channel = await member.guild.channels.fetch('Welcome_Channel_ID')
  channel.send({ files: [card] })
})

client.login('token')
```
And the above should send something like:
![this])(./assets/generate.png)
