# Covid

##                                            Covid Example -

```javascript
client.on('messageCreate', async(message) => {
if(message.content === '!covid'){
const { covid } = require('jelly-djs')
await covid(message, client, 'India')//India is the country you wanna get stats of, defaults to All
}
})
```

### Required Parameters -

| Param | Type | Description |
| :--- | :--- | :--- |
| `Message` | [Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object) | Your message object |
| `Client` | [Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object) | Your client object |

### Optional Parameters -

| Param | Type | Description | Default |
| :--- | :--- | :--- | :--- |
| `Country` | [String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) | The country to get stats of. | ALL/WorldWide |

