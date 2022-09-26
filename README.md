# Due to discords recent update all of theses no longer work.
## Collection of discord console tricks/hacks i found all across the web.
NOTE: If some of the code below is yours (even tho theres so many versions floating around) i dont mean to discredit you sorry :3.

I will continue to update this. If you have any new code that you want on here make a issue with the code and i may add it.

I did not make this code this is a collection of code i found across the web (there were no good repos that included all of them so i made one)

# Extras:

## Account ID's 
Yes you can ban some of them form servers *kinda*

Discord System message account ID: - `643945264868098049`

Discord Community updates account ID - `669627189624307712`

Discord Owner Account ID - `21414249976823808`

Clyde Bots ID - `1`

*Note: Some of them you cant mention because of how IDs work*



## Build Overrides: (Some may be invalid)
Paste this in a channel/dm and click apply

annie/dark: [STILL VALID BUT NO LONGER WORKS] https://discord.com/__development/link?s=Z7XEywE8rsgTvI0MR9P4OknzH4LtPi9j9%2Br8Hwzrohg%3D.eyJ0YXJnZXRCdWlsZE92ZXJyaWRlIjp7ImRpc2NvcmRfd2ViIjp7InR5cGUiOiJicmFuY2giLCJpZCI6ImFubmllL2RhcmsifX0sInJlbGVhc2VDaGFubmVsIjpudWxsLCJ2YWxpZEZvclVzZXJJZHMiOltdLCJhbGxvd0xvZ2dlZE91dCI6ZmFsc2UsImV4cGlyZXNBdCI6IlN1biwgMjggSmFuIDIwMjQgMDE6NTU6MDcgR01UIn0%3D

feature/web-slash-command-localization: https://discord.com/__development/link?s=Z7XEywE8rsgTvI0MR9P4OknzH4LtPi9j9%2Br8Hwzrohg%3D.eyJ0YXJnZXRCdWlsZE92ZXJyaWRlIjp7ImRpc2NvcmRfd2ViIjp7InR5cGUiOiJicmFuY2giLCJpZCI6ImFubmllL2RhcmsifX0sInJlbGVhc2VDaGFubmVsIjpudWxsLCJ2YWxpZEZvclVzZXJJZHMiOltdLCJhbGxvd0xvZ2dlZE91dCI6ZmFsc2UsImV4cGlyZXNBdCI6IlN1biwgMjggSmFuIDIwMjQgMDE6NTU6MDcgR01UIn0%3D

*This only works on desktop and web*


# Discord Console

## Copy your token
```js
window.webpackChunkdiscord_app.push([[Math.random()], {}, (req) => {for (const m of Object.keys(req.c).map((x) => req.c[x].exports).filter((x) => x)) {if (m.default && m.default.getToken !== undefined) {return copy(m.default.getToken())}if (m.getToken !== undefined) {return copy(m.getToken())}}}]);
```


## Log in with a token
```js
function login(token) {
setInterval(() => {
document.body.appendChild(document.createElement `iframe`).contentWindow.localStorage.token = `"${token}"`
}, 50);
setTimeout(() => {
location.reload();
}, 2500);
}

login('PASTE TOKEN HERE')
```

## Get staff public flag (badge)
```js
user = (webpackChunkdiscord_app.push([[''],{},e=>{m=[];for(let c in e.c)m.push(e.c[c])}]),m).find(m => m?.exports?.default?.getCurrentUser).exports.default.getCurrentUser(); user.flags = user.publicFlags += 1;
```


## Get server outage icon at the end of server list
```js
webpackChunkdiscord_app.push([["h"], {}, e => {mods = Object.values(e.c)}]);
for (let [key, val] of Object.entries(mods.find(m => m?.exports?.default?.getGuilds).exports.default.getGuilds())) {
    Dispatcher = (webpackChunkdiscord_app.push([[''],{},e=>{m=[];for(let c in e.c)m.push(e.c[c])}]),m).find(m => m?.exports?.default?.isDispatching)
Dispatcher.exports.default.dispatch({
    type: "GUILD_UNAVAILABLE",
    guildId: val
});
}
```


## Get your currect session ID
```js
(webpackChunkdiscord_app.push([[''],{},e=>{m=[];for(let c in e.c)m.push(e.c[c])}]),m).find(m => m?.exports?.default?.getSessionId).exports.default.getSessionId()
```

## Add phone number to your account.
This does not actually set your number, it just tricks discord thinking it is. You may use letters to. WIll go away after refresh.
```js
window.webpackChunkdiscord_app.push([[Math.random()], {}, (req) => {for (const m of Object.keys(req.c).map((x) => req.c[x].exports).filter((x) => x)) {if (m.default && m.default.getCurrentUser !== undefined) {return m.default.getCurrentUser().phone = '+1NUMBER';}if (m.getCurrentUser !== undefined) {return m.getCurrentUser().phone = '+1NUMBER'}}}]);
window.webpackChunkdiscord_app.push([[Math.random()], {}, (req) => {for (const m of Object.keys(req.c).map((x) => req.c[x].exports).filter((x) => x)) {if (m.default && m.default.getCurrentUser !== undefined) {return m.default.getCurrentUser().verified = true;}if (m.getCurrentUser !== undefined) {return m.getCurrentUser().verified = true}}}]);
```


## Make all servers unavailable
After a refresh it will be back to normal
```js
h='isUnavailable';(webpackChunkdiscord_app.push([[''],{},e=>{m=[];for(let c in e.c)m.push(e.c[c])}]),m).find(m=>m?.exports?.default?.[h]!==void 0).exports.default[h]=(e)=>1
```


## Get all the guilds you are in
```js
(webpackChunkdiscord_app.push([[''],{},e=>{m=[];for(let c in e.c)m.push(e.c[c])}]),m).find(m => m?.exports?.default?.getGuild).exports.default.getGuilds()
```


## Make your friend invite code
Yes that exists
```js
`https://discord.${""}gg/${(await (webpackChunkdiscord_app.push([[''],{},e=>{m=[];for(let c in e.c)m.push(e.c[c])}]),m).find(m => m?.exports?.default?.createFriendInvite).exports.default.createFriendInvite()).code}`
```

## Revoke all friend invites
```js
await (webpackChunkdiscord_app.push([[''],{},e=>{m=[];for(let c in e.c)m.push(e.c[c])}]),m).find(m => m?.exports?.default?.revokeFriendInvites).exports.default.revokeFriendInvites()
```


## Get all your public flags
```js
(webpackChunkdiscord_app.push([[''],{},e=>{m=[];for(let c in e.c)m.push(e.c[c])}]),m).find(m => m?.exports?.default?.getCurrentUser).exports.default.getCurrentUser().publicFlags
```


## Make a desktop notification
```js
(webpackChunkdiscord_app.push([[''],{},e=>{m=[];for(let c in e.c)m.push(e.c[c])}]),m).find(m => m?.exports?.default?.showNotification).exports.default.showNotification('https://cdn.discordapp.com/embed/avatars/0.png', 'Your title', 'Body here', null, {})
```


## Apply annie/dark build override [NO LONGER WORKS]
This will go away after refresh unlike a normal override.
```js
'buildOverride=3ReD%2BC0H5jvQyjL%2BNFqsnQ6XBnuF3rlNR8e3xp2CnSA%3D.eyJkaXNjb3JkX3dlYiI6eyJ0eXBlIjoiYnJhbmNoIiwiaWQiOiJhbm5pZS9kYXJrIn0sIiRtZXRhIjp7ImV4cGlyZXNBdCI6IlN1biwgMjggSmFuIDIwMjQgMDE6NTU6MDcgR01UIn19';
window.location.reload();
```


## Apply feature/web-slash-command-localization build override
This will go away after refresh unlike a normal override.
```js
'buildOverride=VQw65opXPNOuzDRAa9ID91y7BV0U0ATg%2FmZfrhCBCqc%3D.eyJ0YXJnZXRCdWlsZE92ZXJyaWRlIjp7ImRpc2NvcmRfd2ViIjp7InR5cGUiOiJicmFuY2giLCJpZCI6ImZlYXR1cmUvd2ViLXNsYXNoLWNvbW1hbmQtbG9jYWxpemF0aW9uIn19LCJyZWxlYXNlQ2hhbm5lbCI6bnVsbCwidmFsaWRGb3JVc2VySWRzIjpbXSwiYWxsb3dMb2dnZWRPdXQiOmZhbHNlLCJleHBpcmVzQXQiOiJXZWQsIDEwIEF1ZyAyMDIyIDE3OjE4OjQ1IEdNVCJ9';
window.location.reload();
```


## Quarantine Yourself
This does not actually quarantine your account it just tricks discord. Only you can see this and it will go away after reload.
```js
user = (webpackChunkdiscord_app.push([[''],{},e=>{m=[];for(let c in e.c)m.push(e.c[c])}]),m).find(m => m?.exports?.default?.getCurrentUser).exports.default.getCurrentUser(); user.bot = true; user.flags = user.publicFlags = -1;
```

## Give your server all flags
This does not actually give your see\rver that status, it just tricks discord. Only you can see this and it will go away after reload.
You may remove any flag you want and it should stil work.
```js
(webpackChunkdiscord_app.push([[''],{},e=>{m=[];for(let c in e.c)m.push(e.c[c])}]),m).find(m => m?.exports?.default?.getGuild).exports.default.getGuild("<guild_id>").features = new Set(["ROLE_SUBSCRIPTIONS_AVAILABLE_FOR_PURCHASE", "WELCOME_SCREEN_ENABLED", "NEWS", "COMMUNITY", "MEMBER_VERIFICATION_GATE_ENABLED", "PRIVATE_THREADS", "PREVIEW_ENABLED", "SEVEN_DAY_THREAD_ARCHIVE", "THREADS_ENABLED", "THREADS_ENABLED_TESTING", "THREE_DAY_THREAD_ARCHIVE", "VANITY_URL", "PARTNERED", "MONETIZATION_ENABLED", "COMMERCE", "ANIMATED_BANNER", "BANNER", "ROLE_ICONS", "ANIMATED_ICON", "MEMBER_PROFILES", "VIP_REGIONS", "ENABLED_DISCOVERABLE_BEFORE", "MORE_EMOJI", "VERIFIED", "FEATURABLE", "HAS_DIRECTORY_ENTRY", "INVITE_SPLASH", "DISCOVERABLE", "NEW_THREAD_PERMISSIONS", "CHANNEL_BANNER", "TEXT_IN_VOICE_ENABLED", "ROLE_SUBSCRIPTIONS_ENABLED_FOR_PURCHASE", "ROLE_SUBSCRIPTIONS_ENABLED", "PREMIUM_TIER_3_OVERRIDE", "MORE_STICKERS", "RELAY_ENABLED", "INTERNAL_EMPLOYEE_ONLY", "FORCE_RELAY", "TICKETING_ENABLED", "EXPOSED_TO_ACTIVITIES_WTP_EXPERIMENT", "LINKED_TO_HUB", "AUTO_MODERATION", "BOOSTING_TIERS_EXPERIMENT_SMALL_GUILD", "BOOSTING_TIERS_EXPERIMENT_MEDIUM_GUILD", "HAD_EARLY_ACTIVITIES_ACCESS", "TICKETED_EVENTS_ENABLED", "BOT_DEVELOPER_EARLY_ACCESS", "GUILD_HOME_TEST"])
```


## Get guild info
```js
(webpackChunkdiscord_app.push([[''],{},e=>{m=[];for(let c in e.c)m.push(e.c[c])}]),m).find(m => m?.exports?.default?.getGuild).exports.default.getGuild("GUILD_ID")
```



## Get all channels of a guild
```js
((typeof mods === 'undefined' ? webpackChunkdiscord_app.push([["meow"], {}, e => { mods = Object.values(e.c) }]) : null),mods).find(e => e?.exports?.default?.getMutableGuildChannelsForGuild).exports.default.getMutableGuildChannelsForGuild("GUILD_ID")
```



## Get a system tag
```js
window.webpackChunkdiscord_app.push([[Math.random()], {}, (req) => {for (const m of Object.keys(req.c).map((x) => req.c[x].exports).filter((x) => x)) {if (m.default && m.default.getCurrentUser !== undefined) {return m.default.getCurrentUser().isSystemUser = () => true;}if (m.getCurrentUser !== undefined) {return m.getCurrentUser().isSystemUser = () => true}}}])
```


## Get a bot tag
```js
window.webpackChunkdiscord_app.push([[Math.random()], {}, (req) => {for (const m of Object.keys(req.c).map((x) => req.c[x].exports).filter((x) => x)) {if (m.default && m.default.getCurrentUser !== undefined) {return m.default.getCurrentUser().bot = true;}if (m.getCurrentUser !== undefined) {return m.getCurrentUser().bot = true}}}])
```


## Get verified bot tag
```js
window.webpackChunkdiscord_app.push([[Math.random()], {}, (req) => {for (const m of Object.keys(req.c).map((x) => req.c[x].exports).filter((x) => x)) {if (m.default && m.default.getCurrentUser !== undefined) {return m.default.getCurrentUser().isVerifiedBot = () => true;}if (m.getCurrentUser !== undefined) {return m.getCurrentUser().isVerifiedBot = () => true}}}])
```


## Delete a webhook with its url
```js
  let webhookURL = "PUT_WEBHOOK_URL_HERE";  

  await fetch(webhookURL, {
    "method": "DELETE",
  });
```


## Get developer mode
```js
// I will not release the new working code because its how it gets patched faster. To bad so sad
```


## Send clyde error
```js
(webpackChunkdiscord_app.push([[''],{},e=>{m=[];for(let c in e.c)m.push(e.c[c])}]),m).find(m => m?.exports?.default?.sendClydeError).exports.default.sendClydeError("CHANNEL_ID")
```


## Change channel type (in some in some cases setting it to 0 will crash your client)
This does not actually set the channel, it just tricks discord thinking thats the channel type. Only you can see this and it will go away after reload.

Change `.type = 0` to the channel type listed below (Yes 7-9 are non existing dont ask me why)
```js
(webpackChunkdiscord_app.push([[''],{},e=>{m=[];for(let c in e.c)m.push(e.c[c])}]),m).find(m=>m.exports?.default?.hasChannel).exports.default.getChannel("CHANNEL ID").type = 0
```
Channel Types:
> 0 - Text

> 1 - DM

> 2 - Group DM

> 3 - Voice

> 4 - Category 

> 5 - Announcement

> 6 - Store

> 10 - Announcement Thread

> 11 - Public Thread

> 12 - Private Thread

> 13 - Stage

> 14 - Student Hub Directory

> 15 - Forum




# If any of them i listed above dont work anymore then let me know.
