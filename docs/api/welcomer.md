# Base URL
```
https://welcomer.spudjs.repl.co/#
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
const Discord = require('discord.js')
const axios = require('axios')

const client = new Discord.Client({ ... });

client.on('guildMemberAdd', async(member) => {

  const card = await axios.get(`welcomer.spudjs.repl.co/generate?tag=${member.user.tag}&avatar=${member.user.displayAvatarURL({ format: 'png' })}&background=https://i.pinimg.com/originals/90/cd/dc/90cddc7eeddbac6b17b4e25674e9e971.jpg`);
  const channel = await member.guild.channels.fetch('Welcome_Channel_ID');
  
  channel.send({ files: [card] })
})

client.login('token')
```
And the above should send something like:
![](https://welcomer.spudjs.repl.co/generate?tag=</Keita>&background=https://i.pinimg.com/originals/90/cd/dc/90cddc7eeddbac6b17b4e25674e9e971.jpg&avatar=https://cdn.discordapp.com/avatars/814179005515038720/569c2e33f4d3ecbce6008474cc6c6122.png&text1=Welcome%20to%20our%20server%20%3C/Keita%3E&text2=Member%20%2310)

Of course doing it like this is stupidly slow so we've made it a function in the package itself!<br>
If you *don't* want to install the package use the above method (Don't know why you'd want to suffer) Otherwise do the below method

```js
const Discord = require('discord.js');
const axios = require('axios');
const spud = require('spud.js');

const client = new Discord.Client({ options });

client.on('guildMemberAdd', async(member) => {

  const card = new spud.API.welcomer({
    tag: member.user.tag,
    background: 'https://i.pinimg.com/originals/90/cd/dc/90cddc7eeddbac6b17b4e25674e9e971.jpg',
    avatar: member.user.displayAvatarURL({ format: 'png' }),
    text1: `Welcome to our server ${member.user.username}!`,
    text2: `We now have ${member.guild.memberCount} members!`
  })
  const channel = await member.guild.channels.fetch('Welcome_Channel_ID');
  
  channel.send({ files: [card] })
})

client.login('token')
```
And this method has the same output as the above!

And that wraps it up for the welcomer endpoint.


