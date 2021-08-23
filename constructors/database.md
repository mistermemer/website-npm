# Database

##                                      Database Example -

```javascript
const { Database } = require('jelly-djs');
const db = new Database('YOUR_MONGO_URL');
client.on('messageCreate', async(message) => {
if(message.content === '!set){
db.set('test', 'working!');//imagining you set the value first.
} else if(message.content === '!get'){
let data = await db.get('test');
message.reply(data)// -> 'working'
} else if(message.content === '!add'){
db.add('key', 10)//only works if value to be added is a number.
} else if(message.content === '!subtract'){
db.sub('key', 10)//only works if value to be added is a number.
} else if(message.content === '!push'){
db.push('items', ['item1', 'item2'])//only works if the existing value is an array or null.
} else if(message.content === '!pull'){
db.pull('items', 'item1')// -> 'item2', as we pushed 2 items before.
}
})
```

