# Button Calculator

##                                   BUTTON CALCULATOR 

```javascript
const { calculator } = require('jelly-djs');
client.on('messageCreate', async(message) => {
if(message.content === '!calc'){
calculator(message, client)
}
})
```

### Required Paramters -

| Param | Type | Desc |
| :--- | :--- | :--- |
| Message | [Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object) | Your message object |
| Client | [Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object) | Your client object |



