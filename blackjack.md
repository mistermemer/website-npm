---
description: BlackJack - Just like normal blacjack.
---

# BlackJack

##                                         BlackJack Example -

```javascript
const { blackjack } = require("jelly-djs");
client.on('messageCreate', async(msg) => {
  if(msg.content === '!blackjack'){
        
        let game = blackjack(msg, client)
        
        switch (game.result) {
            
          case 'Win':
            // do win stuff here
            break;
          case 'Tie':
            // do tie stuff here
            break;
          case 'Lose':
            // do lose stuff here
            break;
          case 'Double Win':
            // do double win stuff here
            break;
          case 'Double Lose':
            // do double lose stuff here
            break;
          case 'ERROR':
            // do whatever you want
            break;
            
        }
  } 
})
```

### Required Parameters -

| Parameter - | Type | Description |
| :--- | :---: | :---: |
| Message | [Object](https://www.w3schools.com/js/js_objects.asp) | Message variable used in your code |
| Client - | [Object](https://www.w3schools.com/js/js_objects.asp) | Your variable which you used to define your client. |

### Optional Parametres \(Must be inside an object\) -

{% tabs %}
{% tab title="resultEmbed" %}
Name - `resultEmbed`

Type - `boolean`

Description - _If its set to false then your bot will not send any embeds on results, like if an user wins then it will not send anything. Normally its set to false._

Required - `false`
{% endtab %}
{% endtabs %}

### Example with options -

```javascript
const game = await blackjack(message, bot, { resultEmbed: false})//it wont send embeds on results.
switch (game.result) {

        case 'Win':
            message.channel.send({embeds: [
                new Discord.MessageEmbed()
                    .setAuthor(usertag, avatar)
                    .setTitle(`You Win!`)
                    .addField(`Your Hand`, `Cards: ${game.ycontent}\nTotal: \`${game.yvalue}\``)
                    .addField(`My Hand Hand`, `Cards: ${game.dcontent}\nTotal: \`${game.dvalue}\``)
                    .setColor('#26f063')
            ]})

            // do win stuff here

            break;
            //Continue with all the cases.
```

