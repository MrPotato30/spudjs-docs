# Spud.js API

The base URL for the endpoint is:
```
https://spudjs.repl.co/api/
```

As of writing, there only 4 endpoints that have been added!

Most of the current endpoints just require you to fetch;
```js
const axios = require('axios'); // You can use any other package for this

(async () => {

   const fetched = await axios.fetch('https://spudjs.repl.co/api/{enpoint}');
   console.log(fetched.data)

})();
```
## Meme
Fetches a meme from r/memes<br>
Very original 100%
## Food
Generates a random...food image?<br>
I guess you'd need this if you're hungry...
## Welcomer
A fairly customisable welcomer image generator!
For a preview check `welcomer.spudjs.repl.co/generate`<br>
More detailed info in the [docs](https://github.com/MrPotato30/spudjs-docs/blob/main/docs/api/welcomer.md)
## Quote
Gives a random and (probably) famous quote.




