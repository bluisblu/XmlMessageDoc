# XmlMessageDoc

An incomplete list of packet messages used to communicate with the online servers in U.B. Funkeys. Submit an issue or message me on the community discord if any of this information is incorrect in practice.

## Notes

 - By default unless stated that there are child nodes, assume inline xml with a space before the file `/>`, like for example `<a_gpd p="2" />`
 - When playing multiplayer minigames, using chat, or even the galaxy service, the client will append a routing number like for example `1|2|2|0#`, which is the service number, two instances of the plugin number, and then the board/room number. When responding, it is necessary to wrap the response in `<h2_0>{message here}</h2_0>`

## Plugins

 0. [Core](#Core)
 1. [User](#User)
 2. [Chat](#Chat)
 3. [Boxing](#Boxing)
 4. [Mahjongg](#Mahjongg)
 5. [Soccer](#Soccer)
 6. [Pool](#Pool)
 7. [Galaxy](#Galaxy)
 8. [Fight](#Fight)
 9. [Chinese Checkers](#Chinese-Checkers)
 10. [Trunk](#Trunk)
 11. [Worms](#Worms)
 12. [Dominos](#Dominos)
 13. [Multiplayer](#Multiplayer)

## Core

### Client to Server (C2S)

| Actionscript Name         | XML Tag                       | Description                                                                                                  | Example                             |
| ------------------------- | ----------------------------- | ------------------------------------------------------------------------------------------------------------ | ----------------------------------- |
| sendFileListRequest       | [a_gfl](Core-Plugin.md#a_gfl) | `c` - client id                                                                                              |                                     |
| sendPluginDetailsRequest  | [a_gpd](Core-Plugin.md#a_gpd) | `p` - plugin id                                                                                              | `<a_gpd p="7" />`                   |
| sendServiceDetailsRequest | [a_gsd](Core-Plugin.md#a_gsd) | `s` - service id                                                                                             | `<a_gsd s="1" />`                   |
| sendServiceListRequest    | [a_gsl](Core-Plugin.md#a_gsl) | No attributes                                                                                                |                                     |
| sendLoginGuestRequest     | [a_lgu](Core-Plugin.md#a_lgu) | Called when the client and the Arkone service starts<br>`c` - client id<br>`a` - affiliate id<br>`d` - ad id | `<a_lgu d="" a="" c="" />`          |
| sendLoginUserRequest      | [a_lru](Core-Plugin.md#a_lru) | `n` - username<br>`p` - password<br>`l` - constant `1`                                                       | `<a_lru l="1" p="PASS" n="NAME" />` |

### Server to Client (S2C)

| Actionscript Name    | XML Tag                       | Description                                                                                                                           | Example                                                               |
| -------------------- | ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------- |
| onAnotherLogin       | [a_alo](Core-Plugin.md#a_alo) | Opens popup `web_another_login`                                                                                                       |                                                                       |
| onFileListRecieve    | [a_gfl](Core-Plugin.md#a_gfl) | `url` - URL<br>`n` - file name<br>`p` - plugin id<br>`t` - type module<br>`d` - display immediately<br>`o` - popup<br>`c` - closeable |                                                                       |
| onGetPluginDetailes  | [a_gpd](Core-Plugin.md#a_gpd) | `xi` - ip<br>`xp` - port<br>`bi` - backup ip<br>`bp` - backup port<br>`s` - service id<br>`p` - plugin id                             | `<a_gpd xi="127.0.0.1" xp="80" bi="127.0.0.1" bp="80" s="1" p="7" />` |
| onGetServiceDetailes | [a_gsd](Core-Plugin.md#a_gsd) | `xi` - ip<br>`xp` - port<br>`bi` - backup ip<br>`bp` - backup port<br>`s` - service id                                                |                                                                       |
| onGetServiceList     | [a_gsl](Core-Plugin.md#a_gsl) | `xi` - ip<br>`xp` - port<br>`bi` - backup ip<br>`bp` - backup port<br>`id` - service id                                               |                                                                       |
| onUserLogin          | [a_lgu](Core-Plugin.md#a_lgu) | `u` - user id<br>`n` - username<br>`p` - password<br>`s` - service id                                                                 |                                                                       |
| onUserLogin          | [a_lru](Core-Plugin.md#a_lru) | `r` - result ("0" = success)<br>`u` - user id<br>`s` - service id                                                                     |                                                                       |
| setPingTimeout       | [p](Core-Plugin.md#p)         | `t` - time                                                                                                                            |                                                                       |

##  User

### Client to Server (C2S)

| Actionscript Name           | XML Tag                       | Description                                                                                                                                                               | Example |
| --------------------------- | ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------- |
| sendAddBuddy                | [u_abd](User-Plugin.md#u_abd) | `b` - buddy id if arg is a number<br>`n` - the value `else if` arg isn't a string                                                                                         |         |
| sendAddBuddyResponse        | [u_abr](User-Plugin.md#u_abr) | `b` - buddy id if arg is a number<br>`n` - the value `else if` arg isn't a string<br>`r` - answer<br>`a` - reason, if any                                                 |         |
| sendChangingPasswordRquest  | [u_acp](User-Plugin.md#u_acp) | `l` - username<br>`p` - new password<br>`o` - old password                                                                                                                |         |
| sendForgottenPasswordRquest | [u_afp](User-Plugin.md#u_afp) | `l` - username                                                                                                                                                            |         |
| sendChangeChatStatus        | [u_ccs](User-Plugin.md#u_ccs) | `s` - status                                                                                                                                                              |         |
| sendChangePhoneStatus       | [u_cph](User-Plugin.md#u_cph) | `ph` - status                                                                                                                                                             |         |
| sendDeleteBuddy             | [u_dbd](User-Plugin.md#u_dbd) | `b` - buddy id                                                                                                                                                            |         |
| sendDeleteBuddyResponse     | [u_dbr](User-Plugin.md#u_dbr) | `b` - buddy id<br>`n` - name<br>`r` - answer result number                                                                                                                |         |
| sendChangeFlagRequest       | [u_fbd](User-Plugin.md#u_fbd) | `b` - buddy id<br>`bf` - <br>`cf` -                                                                                                                                       |         |
| sendBuddyListRequest        | [u_gbl](User-Plugin.md#u_gbl) | No attributes                                                                                                                                                             |         |
| sendGetBalance              | [u_gcb](User-Plugin.md#u_gcb) | No attributes                                                                                                                                                             |         |
| sendGetCurrencyList         | [u_gcl](User-Plugin.md#u_gcl) | No attributes                                                                                                                                                             |         |
| sendGetFileList             | [u_gfl](User-Plugin.md#u_gfl) | `c` - client id                                                                                                                                                           |         |
| sendGetShortProfileRquest   | [u_gsp](User-Plugin.md#u_gsp) | No attributes                                                                                                                                                             |         |
| sendSecureQuestionRquest    | [u_gsq](User-Plugin.md#u_gsq) | `l` - username                                                                                                                                                            |         |
| sendGetUSAStatesList        | [u_gul](User-Plugin.md#u_gul) | No attributes                                                                                                                                                             |         |
| sendGetFullProfileRquest    | [u_gup](User-Plugin.md#u_gup) | No attributes                                                                                                                                                             |         |
| sendGetUserStatsRquest      | [u_gus](User-Plugin.md#u_gus) | No attributes                                                                                                                                                             |         |
| sendGetCountryList          | [u_gwl](User-Plugin.md#u_gwl) | No attributes                                                                                                                                                             |         |
| sendInvitationResponse      | [u_inr](User-Plugin.md#u_inr) | `f` - from user id<br>`t` - to user id<br>`a` - answer<br>`p` - <br>`bid` - buddy id<br>`gid` - game id                                                                   |         |
| sendInvitation              | [u_inv](User-Plugin.md#u_inv) | `f` - from user id<br>`t` - to user id<br>`p` - <br>`bid` - buddy id<br>`gid` - game id<br>`av` -                                                                         |         |
| sendRegisterUserRequest     | [u_reg](User-Plugin.md#u_reg) | `l` - username<br>`p` - password<br>`c` - client id<br>`a` - affiliate id<br>`d` - ad id<br>Nullable:<br>`email`, `sq`, `sa`, `av`, `cs`, `cm`, `fn`, `ln`, `t`, `b`, `g` |         |
| sendPrivateMsg              | [u_spm](User-Plugin.md#u_spm) | `f` - from user id<br>`t` - to user id<br>`m` - message                                                                                                                   |         |
| sendSaveProfileRequest      | [u_sup](User-Plugin.md#u_sup) | Nullable:<br>`l` - username<br>`p` - password<br>`c` - client id<br>`a` - affiliate id<br>`d` - ad id<br>`email`, `sq`, `sa`, `av`, `cs`, `cm`, `fn`, `ln`, `t`, `b`, `g` |         |

### Server to Client (S2C)

| Actionscript Name         | XML Tag                                                      | Description                                                                                                                                                  | Example |
| ------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------- |
| addBuddy                  | [u_abd](User-Plugin.md#u_abd)                                | `r` - result ("0" = success)<br>`n` - name<br>`a` - activity status<br>`b` - buddy id<br>`o` - online status<br>`s` - status<br>`bf` - <br>`cf` - <br>`ph` - |         |
| addBuddyRequest           | [u_abr](User-Plugin.md#u_abr)                                | `b` - buddy id<br>`n` - name                                                                                                                                 |         |
| onReceiveChangingPassword | [u_acp](User-Plugin.md#u_acp)                                | `r` - result ("0" = success)                                                                                                                                 |         |
| ???                       | [u_afp](User-Plugin.md#u_afp)                                | `r` - result ("0" = success)                                                                                                                                 |         |
| chatStatusBuddy           | [u_ccs](User-Plugin.md#u_ccs)                                | `id` - buddy id<br>`s` - status                                                                                                                              |         |
| onlineStatusBuddy         | [u_cos](User-Plugin.md#u_cos)                                | `id` - buddy id<br>`o` - online status                                                                                                                       |         |
| phoneStatusBuddy          | [u_cph](User-Plugin.md#u_cph)                                | `u` - user id (not sure if buddy)                                                                                                                            |         |
| deleteBuddy               | [u_dbd](User-Plugin.md#u_dbd)                                | `r` - result ("0" = success)<br>`u` - user id<br>`b` - buddy id                                                                                              |         |
| deleteBuddyRequest        | [u_dbr](User-Plugin.md#u_dbr)                                | `n` - buddy name                                                                                                                                             |         |
| flagBuddy                 | [u_fbd](User-Plugin.md#u_fbd)                                | `r` - result ("0" = success)<br>`b` - buddy id<br>`bf` - <br>`cf` -                                                                                          |         |
| receiveBuddyList          | [u_gbl](User-Plugin.md#u_gbl)                                | `r` - result ("0" = success)<br>Array of child nodes:<br>`id` - <br>`n` - name<br>`o` - online status<br>`s` - status<br>`bf` - <br>`cf` - <br>`ph` -        |         |
| ???                       | [u_gcb](User-Plugin.md#u_gcb)                                | Unused                                                                                                                                                       |         |
| ???                       | [u_gcl](User-Plugin.md#u_gcl)                                | Unused                                                                                                                                                       |         |
| onFileListRecieve         | [u_gfl](User-Plugin.md#u_gfl)                                | See a_gfl                                                                                                                                                    |         |
| ???                       | [u_gsp](User-Plugin.md#u_gsp)                                | `r` - result ("0" = success)                                                                                                                                 |         |
| ???                       | [u_gsq](User-Plugin.md#u_gsq)                                | `r` - result ("0" = success)                                                                                                                                 |         |
| ???                       | [u_gth](User-Plugin.md#u_gth)                                | Unused                                                                                                                                                       |         |
| ???                       | [u_gul](User-Plugin.md#u_gul)                                | Unused                                                                                                                                                       |         |
| onReceiveUserProfile      | [u_gup](User-Plugin.md#u_gup)                                | `l` - username<br>`sq` - security question<br>`sa` - security answer                                                                                         |         |
| ???                       | [u_gus](User-Plugin.md#u_gus)                                | `r` - result ("0" = success)                                                                                                                                 |         |
| ???                       | [u_gwl](User-Plugin.md#u_gwl)                                | Unused                                                                                                                                                       |         |
| receiveInvitationResponse | [u_inr](User-Plugin.md#u_inr)                                | `f` - from user<br>`t` - to user                                                                                                                             |         |
| receiveInvitation         | [u_inv](User-Plugin.md#u_inv)                                | `f` - from user<br>`t` - to user                                                                                                                             |         |
| setPingTimeout            | [u_p](User-Plugin.md#u_p)                                    | `t` - time                                                                                                                                                   |         |
| onUserRegistrate          | [u_reg](User-Plugin.md#u_reg)                                | `r` - result ("0" = success)<br>`u` - user id                                                                                                                |         |
| privateMessage            | [u_rpm](User-Plugin.md#u_rpm), [u_spm](User-Plugin.md#u_spm) | `r` - result ("0","1","2" = success)<br>`f` - from user<br>`t` - to user<br>`m` - message                                                                    |         |
| onProfileUpdate           | [u_sup](User-Plugin.md#u_sup)                                | `r` - result ("0" = success)                                                                                                                                 |         |

## Chat

### Client to Server (C2S)

| Actionscript Name                    | XML Tag                 | Description                                                                                                                       | Example |
| ------------------------------------ | ----------------------- | --------------------------------------------------------------------------------------------------------------------------------- | ------- |
| sendChangeProperties                 | [cp](Chat-Plugin.md#cp) | Changes properties, has an inner `pr` element<br>`t` - room type<br>`id` - room id                                                |         |
| sendCreateRoom                       | [cr](Chat-Plugin.md#cr) | Creates a room, has an inner `pr` element<br>`t` - room type                                                                      |         |
| onItemActivate                       | [ia](Chat-Plugin.md#ia) | `o` - count(?)<br>`s` - screen<br>`id` - user id                                                                                  |         |
| sendJoinRoom                         | [jn](Chat-Plugin.md#jn) | Joins a room, has an inner `pr` element<br>`t` - room type<br>`id` - room id                                                      |         |
| sendKickOutFromCrib                  | [ko](Chat-Plugin.md#ko) | `t` - room type<br>`id` - room id<br>`u` - user id                                                                                |         |
| sendChatMsg                          | [ms](Chat-Plugin.md#ms) | `m` - message<br>`t` - room type<br>`id` - room id                                                                                |         |
| onPlayerMove                         | [mv](Chat-Plugin.md#mv) | `n` - node (eg. `n="3:5"`)<br>`s` - screen<br>`id` - user id                                                                      |         |
| onOpenDoor                           | [od](Chat-Plugin.md#od) | `f` - from screen<br>`t` - to screen<br>`id` - user id                                                                            |         |
| onPutItem                            | [pi](Chat-Plugin.md#pi) | `id` - user id<br>`x`, `y` - position<br>`o` - count(?)<br>`s` - scale<br>`sid` - screen                                          |         |
| sendPlayerLocation                   | [pl](Chat-Plugin.md#pl) | `n` - node (eg. `n="3:5"`)<br>`s` - screen<br>`id` - user id<br>`a` - visible                                                     |         |
| sendChangeProperties<br>sendJoinRoom | [pr](Chat-Plugin.md#pr) | May contain inner crib xml data from sendCreateRoom<br>`n` - user name<br>`uid` - user id<br>`f` - funkey id<br>`dl` - dirt level |         |
| onRemoveItem                         | [ri](Chat-Plugin.md#ri) | `s` - screen<br>`o` - count(?)                                                                                                    |         |
| sendEvent                            | [se](Chat-Plugin.md#se) | Sends a special event                                                                                                             |         |

### Server to Client (S2C)

| Actionscript Name           | XML Tag                 | Description                                                                                                                                      | Example |
| --------------------------- | ----------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------ | ------- |
| onReceiveCreatorLeaveCrib   | [cd](Chat-Plugin.md#cd) | `id` - user id                                                                                                                                   |         |
| onReceivePlayerProperties   | [cp](Chat-Plugin.md#cp) | Array of player properties, name attribute may be unnecessary as it gets player by id<br>`uid` - user id<br>`f` - funkey id<br>`dl` - dirt level |         |
| onReceiveCreateRoom         | [cr](Chat-Plugin.md#cr) | `mx` - max guests<br>Special event: <br>`id` - user id                                                                                           |         |
| N/A                         | [ia](Chat-Plugin.md#ia) | Special event: Item activate<br>`id` - user id<br>`o` - count(?)<br>`s` - screen<br>`a` - ?                                                      |         |
| onJoin                      | [jn](Chat-Plugin.md#jn) | `r` - result (0 for success)<br>`id` - room id                                                                                                   |         |
| onReceiveKickOutPlayer      | [ko](Chat-Plugin.md#ko) | `id` - user id                                                                                                                                   |         |
| onReceiveMsg                | [ms](Chat-Plugin.md#ms) | `m` - message<br>`n` - username                                                                                                                  |         |
| N/A                         | [mv](Chat-Plugin.md#mv) | Special event: Other player moved<br>`id` - user id<br>`n` - node (eg. `n="3:5"`)<br>`s` - screen                                                |         |
| N/A                         | [od](Chat-Plugin.md#od) | Special event: Open door<br>`id` - user id<br>`f` - from screen<br>`t` - to screen                                                               |         |
| onReceivePlayerDisconnected | [of](Chat-Plugin.md#of) | `id` - user id                                                                                                                                   |         |
| onReceivePlayerConnected    | [on](Chat-Plugin.md#on) | `id` - user id                                                                                                                                   |         |
| onReceivePlayerRemove       | [pd](Chat-Plugin.md#pd) | `id` - user id                                                                                                                                   |         |
| N/A                         | [pi](Chat-Plugin.md#pi) | Special event: Put item<br>`id` - user id<br>`x`, `y` - position<br>`o` - count(?), nullable<br>`s` - screen, nullable                           |         |
| onReceivePlayerJoin         | [pj](Chat-Plugin.md#pj) | Array of player properties<br>`f` - funkey id<br>`uid` - user id<br>`n` - user name<br>`dl` - dirt level                                         |         |
| N/A                         | [pl](Chat-Plugin.md#pl) | Special event: Receive player location<br>`id` - user id<br>`a` - active (`== 1`)<br>`n` - node (eg. `n="3:5"`)<br>`s` - screen                  |         |
| N/A                         | [ri](Chat-Plugin.md#ri) | Special event: Remove item<br>`o` - count(?)<br>`s` - screen                                                                                     |         |
| onReceiveSpecialEvent       | [se](Chat-Plugin.md#se) | Inner xml nodes are parsed as a special event                                                                                                    |         |

## Boxing

### Client to Server (C2S)

| Actionscript Name | XML Tag                   | Description                                                                                                                                                                                              | Example |
| ----------------- | ------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------- |
| sendAction        | [pe](Boxing-Plugin.md#pe) | `bid` - <br>`e` - action name (`dazed`, `hitUp`, `rest`, `knockedOut`, `dodgeLeft`, `dodgeRight`, `upperCut`, `jabRight`, `jabLeft`, `roundhouseLeft`, `roundhouseRight`, `headButt`)<br>`h` - damage hp |         |

### Server to Client (S2C)

| Actionscript Name | XML Tag                   | Description                                                                                                                                                                                                                                     | Example |
| ----------------- | ------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------- |
| newMPRound        | [nr](Boxing-Plugin.md#nr) | `pl` - player lives<br>`ol` - opponent lives<br>`ph` - player hp<br>`oh` - opponent hp                                                                                                                                                          |         |
| N/A               | [oe](Boxing-Plugin.md#oe) | Receives opponent action and pushes it to stack<br>`e` - action name (`dazed`, `hitUp`, `rest`, `knockedOut`, `dodgeLeft`, `dodgeRight`, `upperCut`, `jabRight`, `jabLeft`, `roundhouseLeft`, `roundhouseRight`, `headButt`)<br>`h` - damage hp |         |
| N/A               | [os](Boxing-Plugin.md#os) | `s` - opponent score                                                                                                                                                                                                                            |         |
| N/A               | [pa](Boxing-Plugin.md#pa) | Play again                                                                                                                                                                                                                                      |         |
| N/A               | [pe](Boxing-Plugin.md#pe) | Receives player action and pushes it to stack<br>`e` - action name (`dazed`, `hitUp`, `rest`, `knockedOut`, `dodgeLeft`, `dodgeRight`, `upperCut`, `jabRight`, `jabLeft`, `roundhouseLeft`, `roundhouseRight`, `headButt`)                      |         |
| N/A               | [pr](Boxing-Plugin.md#pr) | `p` - path<br>`k` - delay kick<br>`d` - delay after dodge<br>`z` - daze delay                                                                                                                                                                   |         |
| N/A               | [ps](Boxing-Plugin.md#ps) | `s` - player score                                                                                                                                                                                                                              |         |

## Mahjongg

### Client to Server (C2S)

| Actionscript Name | XML Tag | Description | Example |
| ----------------- | ------- | ----------- | ------- |
|                   |         |             |         |

### Server to Client (S2C)

| Actionscript Name | XML Tag                     | Description                                        | Example |
| ----------------- | --------------------------- | -------------------------------------------------- | ------- |
| N/A               | [fr](Mahjongg-Plugin.md#fr) | Freeze the game<br>`t` - time                      |         |
| N/A               | [oi](Mahjongg-Plugin.md#oi) | Opponent info update<br>`s` - score<br>`l` - lives |         |
| N/A               | [ot](Mahjongg-Plugin.md#ot) | Opponent's turn<br>`t` - time                      |         |
| N/A               | [pa](Mahjongg-Plugin.md#pa) | Play again                                         |         |
| N/A               | [pi](Mahjongg-Plugin.md#pi) | Player info update<br>`s` - score<br>`l` - lives   |         |
| N/A               | [pt](Mahjongg-Plugin.md#pt) | Player's turn<br>`t` - time                        |         |
| N/A               | [tr](Mahjongg-Plugin.md#tr) | Removes a pair of tiles<br>`x`,`y`, `z` - position |         |
| N/A               | [ts](Mahjongg-Plugin.md#ts) | Resets the tiles<br>`s` - seed                     |         |

## Soccer

### Client to Server (C2S)

| Actionscript Name   | XML Tag                   | Description | Example |
| ------------------- | ------------------------- | ----------- | ------- |
| sendBallSave        | [bs](Soccer-Plugin.md#bs) | N/A         |         |
| sendCharacterChosen | [cc](Soccer-Plugin.md#cc) | N/A         |         |
| sendMoving          | [cm](Soccer-Plugin.md#cm) | N/A         |         |
| sendStrikeParameter | [sp](Soccer-Plugin.md#sp) | N/A         |         |

### Server to Client (S2C)

| Actionscript Name                | XML Tag                   | Description                                                                             | Example |
| -------------------------------- | ------------------------- | --------------------------------------------------------------------------------------- | ------- |
| N/A                              | [bs](Soccer-Plugin.md#bs) | Receive ball state<br>`c` - result<br>`m` - animtype<br>`lx` - x pos<br>`d` - direction |         |
| parseSelected                    | [cc](Soccer-Plugin.md#cc) | `c` - character                                                                         |         |
| serverMoving                     | [cm](Soccer-Plugin.md#cm) | `d` - direction<br>`x` - position                                                       |         |
| startNewRound                    | [nr](Soccer-Plugin.md#nr) | No attributes                                                                           |         |
| parseSelectedOpponent            | [oc](Soccer-Plugin.md#oc) | `c` - character                                                                         |         |
| serverSaidChangeScore (Opponent) | [os](Soccer-Plugin.md#os) | `s` - score                                                                             |         |
| serverPlayAgain                  | [pa](Soccer-Plugin.md#pa) | No attributes                                                                           |         |
| serverSaidChangeScore (Player)   | [ps](Soccer-Plugin.md#ps) | `s` - score                                                                             |         |

## Pool

### Client to Server (C2S)

| Actionscript Name | XML Tag                 | Description                                                                                                                                                                                                                                                                                                                                                          | Example |
| ----------------- | ----------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------- |
| ReleaseCue        | [cs](Pool-Plugin.md#cs) | `bid` - table id<br>`cx` - cue x<br>`a` - rotation<br>`wx` - SaveX<br>`wy` - SaveY<br>`f` - force                                                                                                                                                                                                                                                                    |         |
| ReleaseCue        | [sp](Pool-Plugin.md#sp) | `bid` - table id<br>`dx` - DX<br>`dy` - DY<br>`wx` - SaveX<br>`wy` - SaveY<br>`f` - force<br>`ex` - English X<br>`ey` - English Y<br>`t` - timer<br>`a` - rotation<br><br>Child node: Array of `<b>` balls:<br>`x`, `y` - position<br>`j` - index<br>`s` - is pocketed                                                                                               |         |
| motion_end        | [er](Pool-Plugin.md#er) | `bid` - table id<br>`u` - player's own user id<br>`s` - scratch (1 = cue ball pocketed, 2 = opponent ball pocketed, 3 = didn't hit anything, 4 = opponent's ball first hit, 5 = time's up)<br>`so` - temp pocket 0<br>`st` - temp pocket 1<br>`p` - right pocket<br><br>Child node: Array of `<b>` balls:<br>`x`, `y` - position<br>`i` - index<br>`s` - is pocketed |         |

### Server to Client (S2C)

| Actionscript Name | XML Tag                 | Description                                                                                                                                                               | Example |
| ----------------- | ----------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------- |
| preRollUpdate     | [cs](Pool-Plugin.md#cs) | `wx` - cbX<br>`wy` - cbY<br>`a` - rot<br>`f` - force<br>`cx` - cue pos                                                                                                    |         |
| setStepRight      | [nt](Pool-Plugin.md#nt) | `u` - user id                                                                                                                                                             |         |
| setPlayersScore   | [os](Pool-Plugin.md#os) | `s` - score                                                                                                                                                               |         |
| N/A               | [pa](Pool-Plugin.md#pa) | Play again                                                                                                                                                                |         |
| setChosenPocket   | [pc](Pool-Plugin.md#pc) | `c` - chosen pocket                                                                                                                                                       |         |
| setPlayersScore   | [ps](Pool-Plugin.md#ps) | `s` - score                                                                                                                                                               |         |
| SetPartnerHit     | [sp](Pool-Plugin.md#sp) | `dx` - DX<br>`dy` - DY<br>`wx` - XPOS<br>`wy` - YPOS<br>`f` - POWER<br>`ex` - ENGLISH_X<br>`ey` - ENGLISH_Y<br>`t` - TIMER<br>`a` - CUEROT<br>`cx` - CUEX<br>`p` - POCKET |         |

## Galaxy

### Client to Server (C2S)

| Actionscript Name                  | XML Tag                     | Description | Example |
| ---------------------------------- | --------------------------- | ----------- | ------- |
| sendGetLeaderboardStatisticRequest | [gls](Galaxy-Plugin.md#gls) | N/A         |         |
| sendLoadProfileRequest             | [lp](Galaxy-Plugin.md#lp)   | N/A         |         |
| sendProfileVersionRequest          | [lpv](Galaxy-Plugin.md#lpv) | N/A         |         |
| sendSaveProfileRequest             | [sp](Galaxy-Plugin.md#sp)   | N/A         |         |
| sendSaveProfilePartRequest         | [spp](Galaxy-Plugin.md#spp) | N/A         |         |
| sendStatisticVersionRequest        | [vsu](Galaxy-Plugin.md#vsu) | N/A         |         |

### Server to Client (S2C)

| Actionscript Name              | XML Tag                             | Description                    | Example |
| ------------------------------ | ----------------------------------- | ------------------------------ | ------- |
| onReceiveGalaxyError           | [ge](Galaxy-Plugin.md#ge)           | `r` - result ("-0" = continue) |         |
| onReceiveLeaderboardStatistics | [gls](Galaxy-Plugin.md#gls)         | N/A                            |         |
| onReceiveProfileVersion        | [lpv](Galaxy-Plugin.md#lpv)         | N/A                            |         |
| setPingTimeout                 | [p](Galaxy-Plugin.md#p)             | N/A                            |         |
| onReceiveLoadProfile           | [profile](Galaxy-Plugin.md#profile) | N/A                            |         |
| onReceiveResults               | [rr](Galaxy-Plugin.md#rr)           | N/A                            |         |
| onReceiveSaveProfile           | [sp](Galaxy-Plugin.md#sp)           | N/A                            |         |
| onReceiveStatisticVersion      | [vsu](Galaxy-Plugin.md#vsu)         | N/A                            |         |

## Fight

### Client to Server (C2S)

| Actionscript Name                 | XML Tag                      | Description | Example |
| --------------------------------- | ---------------------------- | ----------- | ------- |
| SEND_Block                        | [bl](Fight-Plugin.md#bl)     | N/A         |         |
| SEND_ExtendedPunch                | [_ep](Fight-Plugin.md#_ep)   | N/A         |         |
| SEND_HeadButt                     | [_hb](Fight-Plugin.md#_hb)   | N/A         |         |
| SEND_HealthReduction              | [_hr](Fight-Plugin.md#_hr)   | N/A         |         |
| SEND_Hit                          | [_ht](Fight-Plugin.md#_ht)   | N/A         |         |
| SEND_JumpKick                     | [_jk](Fight-Plugin.md#_jk)   | N/A         |         |
| SEND_Jump                         | [_jm](Fight-Plugin.md#_jm)   | N/A         |         |
| SEND_JoinGame<br>SEND_JoinGameRTT | [jn](Fight-Plugin.md#jn)     | N/A         |         |
| SEND_Kick                         | [_ki](Fight-Plugin.md#_ki)   | N/A         |         |
| SEND_Move                         | [_mv](Fight-Plugin.md#_mv)   | N/A         |         |
| SEND_Ping                         | [ping](Fight-Plugin.md#ping) | N/A         |         |
| SEND_Punch                        | [_pu](Fight-Plugin.md#_pu)   | N/A         |         |
| SEND_RTT                          | [rtt](Fight-Plugin.md#rtt)   | N/A         |         |
| SEND_SpecialAction                | [_sa](Fight-Plugin.md#_sa)   | N/A         |         |
| SEND_Score                        | [_scr](Fight-Plugin.md#_scr) | N/A         |         |
| SEND_SoftReconciliation           | [_sr](Fight-Plugin.md#_sr)   | N/A         |         |
| SEND_Stop                         | [_st](Fight-Plugin.md#_st)   | N/A         |         |
| SEND_Unblock                      | [ul](Fight-Plugin.md#ul)     | N/A         |         |

### Server to Client (S2C)

| Actionscript Name         | XML Tag                      | Description        | Example |
| ------------------------- | ---------------------------- | ------------------ | ------- |
| MSGHND_ActionAllowance    | [aka](Fight-Plugin.md#aka)   | N/A                |         |
| MSGHND_ActionAllowance    | [akd](Fight-Plugin.md#akd)   | N/A                |         |
| MSGHND_Block              | [bl](Fight-Plugin.md#bl)     | N/A                |         |
| MSGHND_ExtendedPunch      | [_ep](Fight-Plugin.md#_ep)   | N/A                |         |
| MSGHND_ActionAllowance    | [epa](Fight-Plugin.md#epa)   | N/A                |         |
| MSGHND_ActionAllowance    | [epd](Fight-Plugin.md#epd)   | N/A                |         |
| N/A                       | [go](Fight-Plugin.md#go)     | Game over          |         |
| MSGHND_HeadButt           | [_hb](Fight-Plugin.md#_hb)   | N/A                |         |
| MSGHND_HealthReduction    | [_hr](Fight-Plugin.md#_hr)   | N/A                |         |
| MSGHND_Hit                | [_ht](Fight-Plugin.md#_ht)   | N/A                |         |
| MSGHND_JumpKick           | [_jk](Fight-Plugin.md#_jk)   | N/A                |         |
| MSGHND_Jump               | [_jm](Fight-Plugin.md#_jm)   | N/A                |         |
| MSGHND_Join               | [jn](Fight-Plugin.md#jn)     | N/A                |         |
| MSGHND_Kick               | [_ki](Fight-Plugin.md#_ki)   | N/A                |         |
| N/A                       | [lv](Fight-Plugin.md#lv)     | Leave game         |         |
| MSGHND_Move               | [_mv](Fight-Plugin.md#_mv)   | N/A                |         |
| MSGHND_Ping               | [ping](Fight-Plugin.md#ping) | N/A                |         |
| MSGHND_Punch              | [_pu](Fight-Plugin.md#_pu)   | N/A                |         |
| MSGHND_ActionAllowance    | [rka](Fight-Plugin.md#rka)   | N/A                |         |
| MSGHND_ActionAllowance    | [rkd](Fight-Plugin.md#rkd)   | N/A                |         |
| MSGHND_RoundOver          | [ro](Fight-Plugin.md#ro)     | N/A                |         |
| MSGHND_ActionAllowance    | [rpa](Fight-Plugin.md#rpa)   | N/A                |         |
| MSGHND_ActionAllowance    | [rpd](Fight-Plugin.md#rpd)   | N/A                |         |
| MSGHND_SpecialAction      | [_sa](Fight-Plugin.md#_sa)   | N/A                |         |
| N/A                       | [_scr](Fight-Plugin.md#_scr) | Set opponent score |         |
| MSGHND_SoftReconciliation | [_sr](Fight-Plugin.md#_sr)   | N/A                |         |
| MSGHND_Stop               | [_st](Fight-Plugin.md#_st)   | N/A                |         |
| MSGHND_Unblock            | [ul](Fight-Plugin.md#ul)     | N/A                |         |

## Chinese Checkers

### Client to Server (C2S)

| Actionscript Name | XML Tag | Description | Example |
| ----------------- | ------- | ----------- | ------- |

### Server to Client (S2C)

| Actionscript Name       | XML Tag                             | Description | Example |
| ----------------------- | ----------------------------------- | ----------- | ------- |
| receiveMovement         | [mv](Chinese-Checkers-Plugin.md#mv) | N/A         |         |
| receiveTurnNotification | [nt](Chinese-Checkers-Plugin.md#nt) | N/A         |         |
| N/A                     | [pa](Chinese-Checkers-Plugin.md#pa) | Play again  |         |

## Trunk

### Client to Server (C2S)

| Actionscript Name            | XML Tag                      | Description | Example |
| ---------------------------- | ---------------------------- | ----------- | ------- |
| sendAssetParam               | [asp](Trunk-Plugin.md#asp)   | N/A         |         |
| sendBuyCleaning              | [bc](Trunk-Plugin.md#bc)     | N/A         |         |
| sendBuyFamiliar              | [bf](Trunk-Plugin.md#bf)     | N/A         |         |
| sendBuyItem                  | [bi](Trunk-Plugin.md#bi)     | N/A         |         |
| sendBuyJammer                | [bj](Trunk-Plugin.md#bj)     | N/A         |         |
| sendBuyMood                  | [bm](Trunk-Plugin.md#bm)     | N/A         |         |
| sendBuyRoom                  | [br](Trunk-Plugin.md#br)     | N/A         |         |
| sendCleaningsRequest         | [gcl](Trunk-Plugin.md#gcl)   | N/A         |         |
| sendFamiliarsRequest         | [gfl](Trunk-Plugin.md#gfl)   | N/A         |         |
| sendItemsRequest             | [gil](Trunk-Plugin.md#gil)   | N/A         |         |
| sendJammersRequest           | [gjl](Trunk-Plugin.md#gjl)   | N/A         |         |
| sendLootBalanceRequest       | [glb](Trunk-Plugin.md#glb)   | N/A         |         |
| sendMoodsRequest             | [gml](Trunk-Plugin.md#gml)   | N/A         |         |
| sendRoomsRequest             | [grl](Trunk-Plugin.md#grl)   | N/A         |         |
| sendSplashListRequest        | [gsl](Trunk-Plugin.md#gsl)   | N/A         |         |
| sendGetUserAssetRequest      | [gua](Trunk-Plugin.md#gua)   | N/A         |         |
| sendTransactionsRequest      | [gut](Trunk-Plugin.md#gut)   | N/A         |         |
| sendTransactionsCountRequest | [gutc](Trunk-Plugin.md#gutc) | N/A         |         |

### Server to Client (S2C)

| Actionscript Name              | XML Tag                      | Description | Example |
| ------------------------------ | ---------------------------- | ----------- | ------- |
| onReceiveBuyCleaning           | [bc](Trunk-Plugin.md#bc)     | N/A         |         |
| onReceiveBuyFamiliar           | [bf](Trunk-Plugin.md#bf)     | N/A         |         |
| onReceiveBuyItem               | [bi](Trunk-Plugin.md#bi)     | N/A         |         |
| onReceiveBuyJammer             | [bj](Trunk-Plugin.md#bj)     | N/A         |         |
| onReceiveBuyMood               | [bm](Trunk-Plugin.md#bm)     | N/A         |         |
| onReceiveBuyRoom               | [br](Trunk-Plugin.md#br)     | N/A         |         |
| onReceiveCleaningsList         | [gcl](Trunk-Plugin.md#gcl)   | N/A         |         |
| onReceiveFamiliarsList         | [gfl](Trunk-Plugin.md#gfl)   | N/A         |         |
| onReceiveItemsList             | [gil](Trunk-Plugin.md#gil)   | N/A         |         |
| onReceiveJammersList           | [gjl](Trunk-Plugin.md#gjl)   | N/A         |         |
| onReceiveLootBalance           | [glb](Trunk-Plugin.md#glb)   | N/A         |         |
| onReceiveMoodsList             | [gml](Trunk-Plugin.md#gml)   | N/A         |         |
| onReceiveRoomsList             | [grl](Trunk-Plugin.md#grl)   | N/A         |         |
| onReceiveSplashList            | [gsl](Trunk-Plugin.md#gsl)   | N/A         |         |
| onReceiveUserAsset             | [gua](Trunk-Plugin.md#gua)   | N/A         |         |
| onReceiveUserTransactions      | [gut](Trunk-Plugin.md#gut)   | N/A         |         |
| onReceiveUserTransactionsCount | [gutc](Trunk-Plugin.md#gutc) | N/A         |         |
| onReceiveTransactionError      | [te](Trunk-Plugin.md#te)     | N/A         |         |

## Worms

### Client to Server (C2S)

| Actionscript Name | XML Tag | Description | Example |
| ----------------- | ------- | ----------- | ------- |

### Server to Client (S2C)

| Actionscript Name | XML Tag | Description | Example |
| ----------------- | ------- | ----------- | ------- |

## Dominos

### Client to Server (C2S)

| Actionscript Name | XML Tag | Description | Example |
| ----------------- | ------- | ----------- | ------- |

### Server to Client (S2C)

| Actionscript Name | XML Tag | Description | Example |
| ----------------- | ------- | ----------- | ------- |

## Multiplayer

### Client to Server (C2S)

| Actionscript Name       | XML Tag                        | Description | Example |
| ----------------------- | ------------------------------ | ----------- | ------- |
| clickOfferDrawAnswerNo  | [dr](Multiplayer-Plugin.md#dr) | N/A         |         |
| clickOfferDrawAnswerYes | [dw](Multiplayer-Plugin.md#dw) | N/A         |         |
| getFilesPath            | [fp](Multiplayer-Plugin.md#fp) | N/A         |         |
| sendJoin                | [jn](Multiplayer-Plugin.md#jn) | N/A         |         |
| sendLeaveGame           | [lv](Multiplayer-Plugin.md#lv) | N/A         |         |
| sendChatMsg             | [ms](Multiplayer-Plugin.md#ms) | N/A         |         |
| sendPlayAgain           | [pa](Multiplayer-Plugin.md#pa) | N/A         |         |
| sendReadyToGame         | [rp](Multiplayer-Plugin.md#rp) | N/A         |         |

### Server to Client (S2C)

| Actionscript Name | XML Tag                        | Description      | Example |
| ----------------- | ------------------------------ | ---------------- | ------- |
| opponentOfferDraw | [dr](Multiplayer-Plugin.md#dr) | offerdrawdenied  |         |
| opponentOfferDraw | [dw](Multiplayer-Plugin.md#dw) | receiveofferdraw |         |
| loadFiles         | [fp](Multiplayer-Plugin.md#fp) | N/A              |         |
| gameOver          | [go](Multiplayer-Plugin.md#go) | N/A              |         |
| onJoin            | [jn](Multiplayer-Plugin.md#jn) | N/A              |         |
| N/A               | [lv](Multiplayer-Plugin.md#lv) | Leave game       |         |
| onReceiveMsg      | [ms](Multiplayer-Plugin.md#ms) | N/A              |         |
| opponentJoin      | [oj](Multiplayer-Plugin.md#oj) | N/A              |         |
| startGame         | [sg](Multiplayer-Plugin.md#sg) | N/A              |         |
