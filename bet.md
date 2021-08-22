# Betting

##                                     Betting Example -

```javascript
const { bet } = require('jelly-djs')

const game = await bet(message, bot)

    switch (game.output) {

        case 'Win':
            // do win stuff here, you can disable normal win embeds and send your own embeds too.

            break;

        case 'Tie':

            // do tie stuff here

            break;

        case 'Lose':
        
            //do anytyhing if you Loose.

            break;

    }
```

### Required Parameters -

| Parameter - | Type | Description |
| :--- | :--- | :--- |
| `Message` | [Object](https://www.w3schools.com/js/js_object_definition.asp) | Your message object |
| `Client` | [Object](https://www.w3schools.com/js/js_object_definition.asp) | Your client object |

### Optional Parameters -

| Parameter | Type | Description | Default |
| :--- | :--- | :--- | :--- |
| `resultEmbed` | [boolean](https://www.w3schools.com/js/js_booleans.asp) | If set to true, then it will send embeds on win, if false, it wont. | true |

###                                         Betting with options -

```javascript
    const { bet } = require('jelly-djs')
    const game = await bet(message, bot, { resultEmbed: false })

    switch (game.result) {

        case 'Win':
            message.channel.send({embeds: [
                new Discord.MessageEmbed()
                    .setAuthor(usertag, avatar)
                    .setTitle(`You Win!`)
                    .addField(`Your Hand`, `Cards: ${game.ycontent}\nTotal: \`${game.yvalue}\``)
                    .addField(`Jelly's Hand`, `Cards: ${game.dcontent}\nTotal: \`${game.dvalue}\``)
                    .addField(`Ammount Won -`, `${winamt.toLocaleString()}`)
                    .setColor('#26f063')
            ]})
            // do win stuff here

            break;

        case 'Tie':
            message.reply({embeds: [
                new Discord.MessageEmbed()
                    .setAuthor(usertag, avatar)
                    .setTitle(`Match Tied!`)
                    .addField(`Your Hand`, `Cards: ${game.ycontent}\nTotal: \`${game.yvalue}\``)
                    .addField(`Jelly's Hand`, `Cards: ${game.dcontent}\nTotal: \`${game.dvalue}\``)
                    .addField(`Ammount Won -`, `\`0\``)
                    .setColor('YELLOW')
            ]})
            // do tie stuff here

            break;

        case 'Lose':
            message.channel.send({embeds: [
                new Discord.MessageEmbed()
                    .setAuthor(usertag, avatar)
                    .setTitle(`You Loose!`)
                    .addField(`Your Hand`, `Cards: ${game.ycontent}\nTotal: \`${game.yvalue}\``)
                    .addField(`Jelly's Hand`, `Cards: ${game.dcontent}\nTotal: \`${game.dvalue}\``)
                    .addField(`Ammount Lost`, `\`${amt.toLocaleString()}\``)
                    .setColor('#f23518')
            ]})

            // do lose stuff here

            break;
            }

```

