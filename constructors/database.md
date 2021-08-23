# Database

##                                      Database Example -

```javascript
const { Database } = require('jelly-djs');
const db = new Database('YOUR_MONGO_URL');
client.on('messageCreate', async(message) => {
if(message.content === '!set){
db.set('test', 'working!');//imagining you set the value first.
} else if(message.content === '!fetch'){
let data = await db.fetch('test');
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

###                                          FUNCTIONS WITH 2 PARAMS

{% tabs %}
{% tab title="add" %}
Required Params - `key, value`

```javascript
db.add('addition', 500)// -> 500
```
{% endtab %}

{% tab title="sub" %}
Required Params - `key, value`

```javascript
db.sub('subtraction', 500)
/*
if exisitng data was 0 or null then new data = -500
*/

```
{% endtab %}

{% tab title="push" %}
Required Params - `key, value`

```javascript
db.push('pushing', 'PUSH1')
/*
If the exisitng data was [] or null then output = ['PUSH1']
*/

```
{% endtab %}

{% tab title="pull" %}
Required Params - `key, value`

```javascript
db.pull('pushing', 'PUSH1');
/*
Works only if there was an 
```
{% endtab %}
{% endtabs %}

