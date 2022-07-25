# Base URL
```
https://welcomer.spudjs.repl.co/generate
```

### Options
- tag *required
- avatar *required
- text1 *required
- text2 *required
- background *optional
- memberCount *required
- user *required `avatar and tag`
---
#### Example
```js
const { Client } = require('discord.js');
const axios = require('axios');

const client = new Client({ ... });

client.on('guildMemberAdd', async(member) => {
  const card = await axios.get(`welcomer.spudjs.repl.co/generate?tag=${tag}&avatar=${avatar}&background=${background}`);
  const channel = await member.guild.channels.fetch('123456789012345678');
  
  channel.send({ files: [card] });
});

client.login('token');
```
And the above's output will be:
![](https://welcomer.spudjs.repl.co/generate?tag=%3C/Keita%3E&background=https://i.pinimg.com/originals/90/cd/dc/90cddc7eeddbac6b17b4e25674e9e971.jpg&avatar=https://cdn.discordapp.com/avatars/814179005515038720/d6bcf2db8a55e32a7b6115771d4382e3.png&text1=Welcome%20to%20our%20server%20%3C/Keita%3E&text2=Member%20%2310)

Of course, doing it like this is stupidly slow. So we've made it a function in the package itself!<br>
If you *don't* want to install the package, there is no other way but to use the above method (Don't know why you'd want to suffer) Otherwise do the below method

```js
const { Client } = require('discord.js');
const axios = require('axios');
const spud = require('spud.js');

const client = new Client({ options });

client.on('guildMemberAdd', async(member) => {
  const card = new spud.API.welcomer({
    user: user,
    background: background,
    avatar: member.user.avatarURL({ format: 'jpg' }), // Format has to be png or jpg
    text1: `Welcome to our server ${member.user.username}!`,
    memberSize: member.guild.memberCount
  });

  const channel = await member.guild.channels.fetch('Welcome_Channel_ID');
  
  channel.send({
    files: [new Discord.MessageAttachment(card.url, 'welcomer.png')]
   });
});

client.login('token');
```

This wraps it up for the welcomer endpoint.

Simple as that!
