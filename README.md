<div align="center">
  <br />
  <p>
    <a href="https://discord.gg/bRCvFy9"><img src="https://discordapp.com/api/guilds/222078108977594368/embed.png" alt="Discord server" /></a>
    <a href="https://www.npmjs.com/package/discord-rpc"><img src="https://img.shields.io/npm/v/discord-rpc.svg?maxAge=3600" alt="NPM version" /></a>
    <a href="https://www.npmjs.com/package/discord-rpc"><img src="https://img.shields.io/npm/dt/discord-rpc.svg?maxAge=3600" alt="NPM downloads" /></a>
    <a href="https://david-dm.org/discordjs/RPC"><img src="https://img.shields.io/david/discordjs/RPC.svg?maxAge=3600" alt="Dependencies" /></a>
  </p>
  <p>
    <a href="https://nodei.co/npm/discord-rpc/"><img src="https://nodei.co/npm/discord-rpc.png?downloads=true&stars=true" alt="NPM info" /></a>
  </p>
</div>

# Discord.js RPC Extension

### [Documentation](https://discord.js.org/#/docs/rpc/)

### [Rich Presence Example](https://github.com/discordjs/RPC/blob/master/example)

### __Browser__ Example

```javascript
const clientId = '868016688090710067';
const scopes = ['rpc', 'rpc.voice'];

const client = new RPC.Client({ transport: 'ipc' });

client.on('ready', async () => {
  console.log('Logged in as', client.application.name);
  console.log('Authed for user', client.user.username);

  const channel = await RPC.getSelectedVoiceChannel();
});

// Log in to RPC with client id
client.login({ clientId, scopes });
```
