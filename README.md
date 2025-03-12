# XmlMessageDoc

An incomplete list of packet messages used to communicate with the online servers in U.B. Funkeys

## 0 - Core

### Client to Server (C2S)

| Actionscript Name         | XML Tag                       | Description | Plugin | Server Response |
| ------------------------- | ----------------------------- | ----------- | ------ | --------------- |
| sendLoginUserRequest      | [a_lru](Core-Plugin.md#a_lru) | N/A         | Core   | N/A             |
| sendServiceListRequest    | [a_gsl](Core-Plugin.md#a_gsl) | N/A         | Core   | N/A             |
| sendPluginDetailsRequest  | [a_gpd](Core-Plugin.md#a_gpd) | N/A         | Core   | N/A             |
| sendLoginGuestRequest     | [a_lgu](Core-Plugin.md#a_lgu) | N/A         | Core   | N/A             |
| sendFileListRequest       | [a_gfl](Core-Plugin.md#a_gfl) | N/A         | Core   | N/A             |
| sendServiceDetailsRequest | [a_gsd](Core-Plugin.md#a_gsd) | N/A         | Core   | N/A             |

### Server to Client (S2C)

| Actionscript Name    | XML Tag                       | Description | Plugin | Client Response |
| -------------------- | ----------------------------- | ----------- | ------ | --------------- |
| onUserLogin          | [a_lru](Core-Plugin.md#a_lru) | N/A         | Core   | N/A             |
| onGetServiceList     | [a_gsl](Core-Plugin.md#a_gsl) | N/A         | Core   | N/A             |
| onGetPluginDetailes  | [a_gpd](Core-Plugin.md#a_gpd) | N/A         | Core   | N/A             |
| onUserLogin          | [a_lgu](Core-Plugin.md#a_lgu) | N/A         | Core   | N/A             |
| onFileListRecieve    | [a_gfl](Core-Plugin.md#a_gfl) | N/A         | Core   | N/A             |
| onGetServiceDetailes | [a_gsd](Core-Plugin.md#a_gsd) | N/A         | Core   | N/A             |
| onAnotherLogin       | [a_alo](Core-Plugin.md#a_alo) | N/A         | Core   | N/A             |

## 1 - User

### Client to Server (C2S)

|Actionscript Name|XML Tag|Description|Plugin|Server Response|
|---|---|---|---|---|
|sendSaveProfileRequest|[u_sup](User-Plugin.md#u_sup)|N/A|User|N/A|
|sendPrivateMsg|[u_spm](User-Plugin.md#u_spm)|N/A|User|N/A|
|sendRegisterUserRequest|[u_reg](User-Plugin.md#u_reg)|N/A|User|N/A|
|sendInvitationResponse|[u_inr](User-Plugin.md#u_inr)|N/A|User|N/A|
|sendInvitation|[u_inv](User-Plugin.md#u_inv)|N/A|User|N/A|
|sendGetShortProfileRquest|[u_gsp](User-Plugin.md#u_gsp)|N/A|User|N/A|
|sendGetCountryList|[u_gwl](User-Plugin.md#u_gwl)|N/A|User|N/A|
|sendGetFullProfileRquest|[u_gup](User-Plugin.md#u_gup)|N/A|User|N/A|
|sendGetUserStatsRquest|[u_gus](User-Plugin.md#u_gus)|N/A|User|N/A|
|sendGetUSAStatesList|[u_gul](User-Plugin.md#u_gul)|N/A|User|N/A|
|sendGetFileList|[u_gfl](User-Plugin.md#u_gfl)|N/A|User|N/A|
|sendGetCurrencyList|[u_gcl](User-Plugin.md#u_gcl)|N/A|User|N/A|
|sendSecureQuestionRquest|[u_gsq](User-Plugin.md#u_gsq)|N/A|User|N/A|
|sendBuddyListRequest|[u_gbl](User-Plugin.md#u_gbl)|N/A|User|N/A|
|sendChangeFlagRequest|[u_fbd](User-Plugin.md#u_fbd)|N/A|User|N/A|
|sendDeleteBuddyResponse|[u_dbr](User-Plugin.md#u_dbr)|N/A|User|N/A|
|sendGetBalance|[u_gcb](User-Plugin.md#u_gcb)|N/A|User|N/A|
|sendDeleteBuddy|[u_dbd](User-Plugin.md#u_dbd)|N/A|User|N/A|
|sendChangePhoneStatus|[u_cph](User-Plugin.md#u_cph)|N/A|User|N/A|
|sendChangeChatStatus|[u_ccs](User-Plugin.md#u_ccs)|N/A|User|N/A|
|sendChangingPasswordRquest|[u_acp](User-Plugin.md#u_acp)|N/A|User|N/A|
|sendForgottenPasswordRquest|[u_afp](User-Plugin.md#u_afp)|N/A|User|N/A|
|sendAddBuddyResponse|[u_abr](User-Plugin.md#u_abr)|N/A|User|N/A|
|sendAddBuddy|[u_abd](User-Plugin.md#u_abd)|N/A|User|N/A|

### Server to Client (S2C)

|Actionscript Name|XML Tag|Description|Plugin|Client Response|
|---|---|---|---|---|
|onProfileUpdate|[u_sup](User-Plugin.md#u_sup)|N/A|User|N/A|
|onReceivePrivateMsg|[u_spm](User-Plugin.md#u_spm)|N/A|User|N/A|
|onUserRegistrate|[u_reg](User-Plugin.md#u_reg)|N/A|User|N/A|
|onReceivePrivateMsg|[u_rpm](User-Plugin.md#u_rpm)|N/A|User|N/A|
|onReceiveInvitationResponse|[u_inr](User-Plugin.md#u_inr)|N/A|User|N/A|
|setPingTimeout|[u_p](User-Plugin.md#u_p)|N/A|User|N/A|
|onReceiveInvitation|[u_inv](User-Plugin.md#u_inv)|N/A|User|N/A|
|???|[u_gsp](User-Plugin.md#u_gsp)|N/A|User|N/A|
|???|[u_gwl](User-Plugin.md#u_gwl)|N/A|User|N/A|
|onReceiveUserProfile|[u_gup](User-Plugin.md#u_gup)|N/A|User|N/A|
|???|[u_gus](User-Plugin.md#u_gus)|N/A|User|N/A|
|???|[u_gul](User-Plugin.md#u_gul)|N/A|User|N/A|
|onFileListRecieve|[u_gfl](User-Plugin.md#u_gfl)|N/A|User|N/A|
|???|[u_gcl](User-Plugin.md#u_gcl)|N/A|User|N/A|
|???|[u_gth](User-Plugin.md#u_gth)|N/A|User|N/A|
|???|[u_gsq](User-Plugin.md#u_gsq)|N/A|User|N/A|
|onReceiveBuddyList|[u_gbl](User-Plugin.md#u_gbl)|N/A|User|N/A|
|onReceiveFlagBuddy|[u_fbd](User-Plugin.md#u_fbd)|N/A|User|N/A|
|onReceiveDeleteBuddyRequest|[u_dbr](User-Plugin.md#u_dbr)|N/A|User|N/A|
|???|[u_gcb](User-Plugin.md#u_gcb)|N/A|User|N/A|
|onReceiveDeleteBuddy|[u_dbd](User-Plugin.md#u_dbd)|N/A|User|N/A|
|onReceiveChangePhoneStatus|[u_cph](User-Plugin.md#u_cph)|N/A|User|N/A|
|onReceiveChatStatusBuddy|[u_ccs](User-Plugin.md#u_ccs)|N/A|User|N/A|
|onReceiveOnlineStatusBuddy|[u_cos](User-Plugin.md#u_cos)|N/A|User|N/A|
|onReceiveChangingPassword|[u_acp](User-Plugin.md#u_acp)|N/A|User|N/A|
|???|[u_afp](User-Plugin.md#u_afp)|N/A|User|N/A|
|onReceiveAddBuddyRequest|[u_abr](User-Plugin.md#u_abr)|N/A|User|N/A|
|onReceiveAddBuddy|[u_abd](User-Plugin.md#u_abd)|N/A|User|N/A|

## 2 - Chat

### Client to Server (C2S)

|Actionscript Name|XML Tag|Description|Plugin|Server Response|
|---|---|---|---|---|
|sendEvent|[se](Chat-Plugin.md#se)|N/A|Chat|N/A|
|sendPlayerLocation|[pl](Chat-Plugin.md#pl)|N/A|Chat|N/A|
|onOpenDoor|[od](Chat-Plugin.md#od)|N/A|Chat|N/A|
|onPlayerMove|[mv](Chat-Plugin.md#mv)|N/A|Chat|N/A|
|sendChatMsg|[ms](Chat-Plugin.md#ms)|N/A|Multiplayer, Chat|N/A|
|sendKickOutFromCrib|[ko](Chat-Plugin.md#ko)|N/A|Chat|N/A|
|sendJoin (Multiplayer), sendJoinRoom (Chat), SEND_JoinGame (Fight), SEND_JoinGameRTT (Fight)|[jn](Chat-Plugin.md#jn)|N/A|Multiplayer, Chat, Fight|N/A|
|onItemActivate|[ia](Chat-Plugin.md#ia)|N/A|Chat|N/A|
|sendCreateRoom|[cr](Chat-Plugin.md#cr)|N/A|Chat|N/A|
|sendChangeProperties|[cp](Chat-Plugin.md#cp)|N/A|Chat|N/A|
|onPutItem|[pi](Chat-Plugin.md#pi)|N/A|Chat|N/A|
|onRemoveItem|[ri](Chat-Plugin.md#ri)|N/A|Chat|N/A|

### Server to Client (S2C)

| Actionscript Name           | XML Tag                    | Description                                                                                                                               | Plugin                   | Client Response |
| --------------------------- | -------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ------------------------ | --------------- |
| onReceiveSpecialEvent       | [se](Chat-Plugin.md#se) | N/A                                                                                                                                       | Chat                     | N/A             |
| N/A                         | [pl](Chat-Plugin.md#pl) | Receive player location                                                                                                                   | Chat                     | N/A             |
| onReceivePlayerList         | [pj](Chat-Plugin.md#pj) | N/A                                                                                                                                       | Chat                     | N/A             |
| onReceivePlayerRemove       | [pd](Chat-Plugin.md#pd) | N/A                                                                                                                                       | Chat                     | N/A             |
| setPingTimeout              | [p](Chat-Plugin.md#p)   | N/A                                                                                                                                       | Galaxy, Chat             | N/A             |
| onReceivePlayerConnected    | [on](Chat-Plugin.md#on) | N/A                                                                                                                                       | Chat                     | N/A             |
| onReceivePlayerDisconnected | [of](Chat-Plugin.md#of) | N/A                                                                                                                                       | Chat                     | N/A             |
| onReceiveMsg                | [ms](Chat-Plugin.md#ms) | N/A                                                                                                                                       | Multiplayer, Chat        | N/A             |
| onReceiveKickOutPlayer      | [ko](Chat-Plugin.md#ko) | N/A                                                                                                                                       | Chat                     | N/A             |
| onJoin, MSGHND_Join (Fight) | [jn](Chat-Plugin.md#jn) | N/A                                                                                                                                       | Multiplayer, Chat, Fight | N/A             |
| onReceiveCreateRoom         | [cr](Chat-Plugin.md#cr) | N/A                                                                                                                                       | Chat                     | N/A             |
| onReceivePlayerProperties   | [cp](Chat-Plugin.md#cp) | N/A                                                                                                                                       | Chat                     | N/A             |
| onReceiveCreatorLeaveCrib   | [cd](Chat-Plugin.md#cd) | N/A                                                                                                                                       | Chat                     | N/A             |
| N/A                         | [pi](Chat-Plugin.md#pi) | Player's turn ends because they didn't make a make before the timer ended (Mahjongg), Calls "putItemForChat" on the current screen (Chat) | Mahjongg, Chat           | N/A             |
| N/A                         | [ri](Chat-Plugin.md#ri) | Calls "removeItemForChat" on the current screen                                                                                           | Chat                     | N/A             |

## 3 - Boxing

### Client to Server (C2S)

|Actionscript Name|XML Tag|Description|Plugin|Server Response|
|---|---|---|---|---|
|sendAction|[pe](Boxing-Plugin.md#pe)|N/A|Boxing|N/A|

### Server to Client (S2C)

|Actionscript Name|XML Tag|Description|Plugin|Client Response|
|---|---|---|---|---|
|serverSaidChangeScore (Player) (Soccer), setPlayersScore (Player) (Pool)|[ps](Boxing-Plugin.md#ps)|N/A|Soccer, Boxing, Pool|N/A|
|N/A|[pe](Boxing-Plugin.md#pe)|Receives player action and pushes it to stack|Boxing|N/A|
|serverPlayAgain (Soccer)|[pa](Boxing-Plugin.md#pa)|Play again|Soccer, Mahjongg, Boxing, Pool, Chinese Checkers|N/A|
|serverSaidChangeScore (Opponent) (Soccer), setPlayersScore (Opponent) (Pool)|[os](Boxing-Plugin.md#os)|N/A|Soccer, Boxing|N/A|
|N/A|[oe](Boxing-Plugin.md#oe)|Receives opponent action and pushes it to stack|Boxing|N/A|
|startNewRound (Soccer), newMPRound (Boxing)|[nr](Boxing-Plugin.md#nr)|N/A|Soccer, Boxing|N/A|

## 4 - Mahjongg

### Client to Server (C2S)

|Actionscript Name|XML Tag|Description|Plugin|Server Response|
|---|---|---|---|---|

### Server to Client (S2C)

|Actionscript Name|XML Tag|Description|Plugin|Client Response|
|---|---|---|---|---|
|N/A|[ts](Mahjongg-Plugin.md#ts)|N/A|Mahjongg|N/A|
|N/A|[tr](Mahjongg-Plugin.md#tr)|Removes a pair of tiles|Mahjongg|N/A|
|N/A|[pt](Mahjongg-Plugin.md#pt)|Player's turn|Mahjongg|N/A|
|serverPlayAgain (Soccer)|[pa](Mahjongg-Plugin.md#pa)|Play again|Soccer, Mahjongg, Boxing, Pool, Chinese Checkers|N/A|
|N/A|[ot](Mahjongg-Plugin.md#ot)|Opponent's turn|Mahjongg|N/A|
|N/A|[oi](Mahjongg-Plugin.md#oi)|Opponent's turn ends because they didn't make a make before the timer ended|Mahjongg|N/A|
|N/A|[fr](Mahjongg-Plugin.md#fr)|Freeze the game for `t` milliseconds(?)|Mahjongg|N/A|
|N/A|[pi](Mahjongg-Plugin.md#pi)|Player's turn ends because they didn't make a make before the timer ended (Mahjongg), Calls "putItemForChat" on the current screen (Chat)|Mahjongg, Chat|N/A|

## 5 - Soccer

### Client to Server (C2S)

| Actionscript Name                                             | XML Tag                    | Description | Plugin         | Server Response |
| ------------------------------------------------------------- | -------------------------- | ----------- | -------------- | --------------- |
| sendSaveProfileRequest (Galaxy), sendStrikeParameter (Soccer) | [sp](Soccer-Plugin.md#sp) | N/A         | Galaxy, Soccer | N/A             |
| sendMoving                                                    | [cm](Soccer-Plugin.md#cm) | N/A         | Soccer         | N/A             |
| sendBallSave                                                  | [bs](Soccer-Plugin.md#bs) | N/A         | Soccer         | N/A             |
| sendCharacterChosen                                           | [cc](Soccer-Plugin.md#cc) | N/A         | Soccer         | N/A             |

### Server to Client (S2C)

|Actionscript Name|XML Tag|Description|Plugin|Client Response|
|---|---|---|---|---|
|serverSaidChangeScore (Player) (Soccer), setPlayersScore (Player) (Pool)|[ps](Soccer-Plugin.md#ps)|N/A|Soccer, Boxing, Pool|N/A|
|serverPlayAgain (Soccer)|[pa](Soccer-Plugin.md#pa)|Play again|Soccer, Mahjongg, Boxing, Pool, Chinese Checkers|N/A|
|serverSaidChangeScore (Opponent) (Soccer), setPlayersScore (Opponent) (Pool)|[os](Soccer-Plugin.md#os)|N/A|Soccer, Boxing|N/A|
|startNewRound (Soccer), newMPRound (Boxing)|[nr](Soccer-Plugin.md#nr)|N/A|Soccer, Boxing|N/A|
|parseSelectedOpponent|[oc](Soccer-Plugin.md#oc)|N/A|Soccer|N/A|
|serverMoving|[cm](Soccer-Plugin.md#cm)|N/A|Soccer|N/A|
|N/A|[bs](Soccer-Plugin.md#bs)|Receive ball state|Soccer|N/A|
|parseSelected|[cc](Soccer-Plugin.md#cc)|N/A|Soccer|N/A|

## 6 - Pool

### Client to Server (C2S)

|Actionscript Name|XML Tag|Description|Plugin|Server Response|
|---|---|---|---|---|

### Server to Client (S2C)

|Actionscript Name|XML Tag|Description|Plugin|Client Response|
|---|---|---|---|---|
|onReceiveSaveProfile (Galaxy), SetPartnerHit (Pool)|[sp](Pool-Plugin.md#sp)|N/A|Galaxy, Pool|N/A|
|serverSaidChangeScore (Player) (Soccer), setPlayersScore (Player) (Pool)|[ps](Pool-Plugin.md#ps)|N/A|Soccer, Boxing, Pool|N/A|
|setChosenPocket|[pc](Pool-Plugin.md#pc)|N/A|Pool|N/A|
|serverPlayAgain (Soccer)|[pa](Pool-Plugin.md#pa)|Play again|Soccer, Mahjongg, Boxing, Pool, Chinese Checkers|N/A|
|setStepRight (Pool), receiveTurnNotification (Chinese Checkers)|[nt](Pool-Plugin.md#nt)|N/A|Pool, Chinese Checkers|N/A|
|preRollUpdate|[cs](Pool-Plugin.md#cs)|N/A|Pool|N/A|

## 7 - Galaxy

### Client to Server (C2S)

| Actionscript Name                                             | XML Tag                      | Description | Plugin         | Server Response |
| ------------------------------------------------------------- | ---------------------------- | ----------- | -------------- | --------------- |
| sendStatisticVersionRequest                                   | [vsu](Galaxy-Plugin.md#vsu) | N/A         | Galaxy         | N/A             |
| sendSaveProfileRequest (Galaxy), sendStrikeParameter (Soccer) | [sp](Galaxy-Plugin.md#sp)   | N/A         | Galaxy, Soccer | N/A             |
| sendSaveProfilePartRequest                                    | [spp](Galaxy-Plugin.md#spp) | N/A         | Galaxy         | N/A             |
| sendProfileVersionRequest                                     | [lpv](Galaxy-Plugin.md#lpv) | N/A         | Galaxy         | N/A             |
| sendLoadProfileRequest                                        | [lp](Galaxy-Plugin.md#lp)   | N/A         | Galaxy         | N/A             |
| sendGetLeaderboardStatisticRequest                            | [gls](Galaxy-Plugin.md#gls) | N/A         | Galaxy         | N/A             |

### Server to Client (S2C)

|Actionscript Name|XML Tag|Description|Plugin|Client Response|
|---|---|---|---|---|
|onReceiveStatisticVersion|[vsu](Galaxy-Plugin.md#vsu)|N/A|Galaxy|N/A|
|onReceiveSaveProfile (Galaxy), SetPartnerHit (Pool)|[sp](Galaxy-Plugin.md#sp)|N/A|Galaxy, Pool|N/A|
|onReceiveResults|[rr](Galaxy-Plugin.md#rr)|N/A|Galaxy|N/A|
|onReceiveLoadProfile|[profile](Galaxy-Plugin.md#profile)|N/A|Galaxy|N/A|
|setPingTimeout|[p](Galaxy-Plugin.md#p)|N/A|Galaxy, Chat|N/A|
|onReceiveProfileVersion|[lpv](Galaxy-Plugin.md#lpv)|N/A|Galaxy|N/A|
|onReceiveLeaderboardStatistics|[gls](Galaxy-Plugin.md#gls)|N/A|Galaxy|N/A|
|onReceiveGalaxyError|[ge](Galaxy-Plugin.md#ge)|N/A|Galaxy|N/A|

## 8 - Fight

### Client to Server (C2S)

| Actionscript Name                                                                            | XML Tag                        | Description | Plugin                   | Server Response |
| -------------------------------------------------------------------------------------------- | ------------------------------ | ----------- | ------------------------ | --------------- |
| SEND_Punch                                                                                   | [_pu](Fight-Plugin.md#_pu)   | N/A         | Fight                    | N/A             |
| SEND_Move                                                                                    | [_mv](Fight-Plugin.md#_mv)   | N/A         | Fight                    | N/A             |
| SEND_Stop                                                                                    | [_st](Fight-Plugin.md#_st)   | N/A         | Fight                    | N/A             |
| SEND_SoftReconciliation                                                                      | [_sr](Fight-Plugin.md#_sr)   | N/A         | Fight                    | N/A             |
| SEND_Score                                                                                   | [_scr](Fight-Plugin.md#_scr) | N/A         | Fight                    | N/A             |
| SEND_SpecialAction                                                                           | [_sa](Fight-Plugin.md#_sa)   | N/A         | Fight                    | N/A             |
| SEND_Hit                                                                                     | [_ht](Fight-Plugin.md#_ht)   | N/A         | Fight                    | N/A             |
| SEND_Jump                                                                                    | [_jm](Fight-Plugin.md#_jm)   | N/A         | Fight                    | N/A             |
| SEND_Kick                                                                                    | [_ki](Fight-Plugin.md#_ki)   | N/A         | Fight                    | N/A             |
| SEND_ExtendedPunch                                                                           | [_ep](Fight-Plugin.md#_ep)   | N/A         | Fight                    | N/A             |
| SEND_JumpKick                                                                                | [_jk](Fight-Plugin.md#_jk)   | N/A         | Fight                    | N/A             |
| SEND_HealthReduction                                                                         | [_hr](Fight-Plugin.md#_hr)   | N/A         | Fight                    | N/A             |
| SEND_HeadButt                                                                                | [_hb](Fight-Plugin.md#_hb)   | N/A         | Fight                    | N/A             |
| SEND_Unblock                                                                                 | [ul](Fight-Plugin.md#ul)     | N/A         | Fight                    | N/A             |
| SEND_RTT                                                                                     | [rtt](Fight-Plugin.md#rtt)   | N/A         | Fight                    | N/A             |
| SEND_Ping                                                                                    | [ping](Fight-Plugin.md#ping) | N/A         | Fight                    | N/A             |
| sendJoin (Multiplayer), sendJoinRoom (Chat), SEND_JoinGame (Fight), SEND_JoinGameRTT (Fight) | [jn](Fight-Plugin.md#jn)     | N/A         | Multiplayer, Chat, Fight | N/A             |
| SEND_Block                                                                                   | [bl](Fight-Plugin.md#bl)     | N/A         | Fight                    | N/A             |

### Server to Client (S2C)

|Actionscript Name|XML Tag|Description|Plugin|Client Response|
|---|---|---|---|---|
|MSGHND_Punch|[_pu](Fight-Plugin.md#_pu)|N/A|Fight|N/A|
|MSGHND_Move|[_mv](Fight-Plugin.md#_mv)|N/A|Fight|N/A|
|MSGHND_Stop|[_st](Fight-Plugin.md#_st)|N/A|Fight|N/A|
|MSGHND_SoftReconciliation|[_sr](Fight-Plugin.md#_sr)|N/A|Fight|N/A|
|N/A|[_scr](Fight-Plugin.md#_scr)|Set opponent score|Fight|N/A|
|MSGHND_SpecialAction|[_sa](Fight-Plugin.md#_sa)|N/A|Fight|N/A|
|MSGHND_Hit|[_ht](Fight-Plugin.md#_ht)|N/A|Fight|N/A|
|MSGHND_Jump|[_jm](Fight-Plugin.md#_jm)|N/A|Fight|N/A|
|MSGHND_Kick|[_ki](Fight-Plugin.md#_ki)|N/A|Fight|N/A|
|MSGHND_ExtendedPunch|[_ep](Fight-Plugin.md#_ep)|N/A|Fight|N/A|
|MSGHND_JumpKick|[_jk](Fight-Plugin.md#_jk)|N/A|Fight|N/A|
|MSGHND_HealthReduction|[_hr](Fight-Plugin.md#_hr)|N/A|Fight|N/A|
|MSGHND_HeadButt|[_hb](Fight-Plugin.md#_hb)|N/A|Fight|N/A|
|MSGHND_Unblock|[ul](Fight-Plugin.md#ul)|N/A|Fight|N/A|
|MSGHND_ActionAllowance|[rpd](Fight-Plugin.md#rpd)|N/A|Fight|N/A|
|MSGHND_ActionAllowance|[rpa](Fight-Plugin.md#rpa)|N/A|Fight|N/A|
|MSGHND_ActionAllowance|[rka](Fight-Plugin.md#rka)|N/A|Fight|N/A|
|MSGHND_RoundOver|[ro](Fight-Plugin.md#ro)|N/A|Fight|N/A|
|MSGHND_ActionAllowance|[rkd](Fight-Plugin.md#rkd)|N/A|Fight|N/A|
|MSGHND_Ping|[ping](Fight-Plugin.md#ping)|N/A|Fight|N/A|
|N/A|[lv](Fight-Plugin.md#lv)|N/A|Fight|N/A|
|onJoin, MSGHND_Join (Fight)|[jn](Fight-Plugin.md#jn)|N/A|Multiplayer, Chat, Fight|N/A|
|gameOver (Multiplayer)|[go](Fight-Plugin.md#go)|N/A|Multiplayer, Fight|N/A|
|MSGHND_ActionAllowance|[epd](Fight-Plugin.md#epd)|N/A|Fight|N/A|
|MSGHND_ActionAllowance|[epa](Fight-Plugin.md#epa)|N/A|Fight|N/A|
|MSGHND_Block|[bl](Fight-Plugin.md#bl)|N/A|Fight|N/A|
|MSGHND_ActionAllowance|[akd](Fight-Plugin.md#akd)|N/A|Fight|N/A|
|MSGHND_ActionAllowance|[aka](Fight-Plugin.md#aka)|N/A|Fight|N/A|

## 9 - Chinese Checkers

### Client to Server (C2S)

|Actionscript Name|XML Tag|Description|Plugin|Server Response|
|---|---|---|---|---|

### Server to Client (S2C)

| Actionscript Name                                               | XML Tag                    | Description | Plugin                                           | Client Response |
| --------------------------------------------------------------- | -------------------------- | ----------- | ------------------------------------------------ | --------------- |
| serverPlayAgain (Soccer)                                        | [pa](Chinese-Checkers-Plugin.md#pa) | Play again  | Soccer, Mahjongg, Boxing, Pool, Chinese Checkers | N/A             |
| setStepRight (Pool), receiveTurnNotification (Chinese Checkers) | [nt](Chinese-Checkers-Plugin.md#nt) | N/A         | Pool, Chinese Checkers                           | N/A             |
| receiveMovement                                                 | [mv](Chinese-Checkers-Plugin.md#mv) | N/A         | Chinese Checkers                                 | N/A             |

## 10 - Trunk

### Client to Server (C2S)

|Actionscript Name|XML Tag|Description|Plugin|Server Response|
|---|---|---|---|---|
|sendTransactionsRequest|[gut](Trunk-Plugin.md#gut)|N/A|Trunk|N/A|
|sendTransactionsCountRequest|[gutc](Trunk-Plugin.md#gutc)|N/A|Trunk|N/A|
|sendGetUserAssetRequest|[gua](Trunk-Plugin.md#gua)|N/A|Trunk|N/A|
|sendSplashListRequest|[gsl](Trunk-Plugin.md#gsl)|N/A|Trunk|N/A|
|sendMoodsRequest|[gml](Trunk-Plugin.md#gml)|N/A|Trunk|N/A|
|sendRoomsRequest|[grl](Trunk-Plugin.md#grl)|N/A|Trunk|N/A|
|sendLootBalanceRequest|[glb](Trunk-Plugin.md#glb)|N/A|Trunk|N/A|
|sendJammersRequest|[gjl](Trunk-Plugin.md#gjl)|N/A|Trunk|N/A|
|sendItemsRequest|[gil](Trunk-Plugin.md#gil)|N/A|Trunk|N/A|
|sendFamiliarsRequest|[gfl](Trunk-Plugin.md#gfl)|N/A|Trunk|N/A|
|sendCleaningsRequest|[gcl](Trunk-Plugin.md#gcl)|N/A|Trunk|N/A|
|sendBuyRoom|[br](Trunk-Plugin.md#br)|N/A|Trunk|N/A|
|sendBuyMood|[bm](Trunk-Plugin.md#bm)|N/A|Trunk|N/A|
|sendBuyItem|[bi](Trunk-Plugin.md#bi)|N/A|Trunk|N/A|
|sendBuyJammer|[bj](Trunk-Plugin.md#bj)|N/A|Trunk|N/A|
|sendBuyFamiliar|[bf](Trunk-Plugin.md#bf)|N/A|Trunk|N/A|
|sendBuyCleaning|[bc](Trunk-Plugin.md#bc)|N/A|Trunk|N/A|
|sendAssetParam|[asp](Trunk-Plugin.md#asp)|N/A|Trunk|N/A|

### Server to Client (S2C)

|Actionscript Name|XML Tag|Description|Plugin|Client Response|
|---|---|---|---|---|
|onReceiveTransactionError|[te](Trunk-Plugin.md#te)|N/A|Trunk|N/A|
|onReceiveUserTransactions|[gut](Trunk-Plugin.md#gut)|N/A|Trunk|N/A|
|onReceiveUserTransactionsCount|[gutc](Trunk-Plugin.md#gutc)|N/A|Trunk|N/A|
|onReceiveUserAsset|[gua](Trunk-Plugin.md#gua)|N/A|Trunk|N/A|
|onReceiveSplashList|[gsl](Trunk-Plugin.md#gsl)|N/A|Trunk|N/A|
|onReceiveMoodsList|[gml](Trunk-Plugin.md#gml)|N/A|Trunk|N/A|
|onReceiveRoomsList|[grl](Trunk-Plugin.md#grl)|N/A|Trunk|N/A|
|onReceiveLootBalance|[glb](Trunk-Plugin.md#glb)|N/A|Trunk|N/A|
|onReceiveJammersList|[gjl](Trunk-Plugin.md#gjl)|N/A|Trunk|N/A|
|onReceiveItemsList|[gil](Trunk-Plugin.md#gil)|N/A|Trunk|N/A|
|onReceiveFamiliarsList|[gfl](Trunk-Plugin.md#gfl)|N/A|Trunk|N/A|
|onReceiveCleaningsList|[gcl](Trunk-Plugin.md#gcl)|N/A|Trunk|N/A|
|onReceiveBuyRoom|[br](Trunk-Plugin.md#br)|N/A|Trunk|N/A|
|onReceiveBuyMood|[bm](Trunk-Plugin.md#bm)|N/A|Trunk|N/A|
|onReceiveBuyItem|[bi](Trunk-Plugin.md#bi)|N/A|Trunk|N/A|
|onReceiveBuyJammer|[bj](Trunk-Plugin.md#bj)|N/A|Trunk|N/A|
|onReceiveBuyFamiliar|[bf](Trunk-Plugin.md#bf)|N/A|Trunk|N/A|
|onReceiveBuyCleaning|[bc](Trunk-Plugin.md#bc)|N/A|Trunk|N/A|

## 11 - Worms

### Client to Server (C2S)

|Actionscript Name|XML Tag|Description|Plugin|Server Response|
|---|---|---|---|---|

### Server to Client (S2C)

|Actionscript Name|XML Tag|Description|Plugin|Client Response|
|---|---|---|---|---|

## 12 - Dominos

### Client to Server (C2S)

| Actionscript Name | XML Tag | Description | Plugin | Server Response |
| ----------------- | ------- | ----------- | ------ | --------------- |

### Server to Client (S2C)

|Actionscript Name|XML Tag|Description|Plugin|Client Response|
|---|---|---|---|---|
