# XmlMessageDoc

An incomplete list of packet messages used to communicate with the online servers in U.B. Funkeys

## 0 - Core

### Client to Server (C2S)

| Actionscript Name         | XML Tag                       | Description | Plugin | Server Response |
| ------------------------- | ----------------------------- | ----------- | ------ | --------------- |
| sendLoginUserRequest      | [a_lru](Core Plugin#a_lru) | N/A         | Core   | N/A             |
| sendServiceListRequest    | [a_gsl](Core Plugin#a_gsl) | N/A         | Core   | N/A             |
| sendPluginDetailsRequest  | [a_gpd](Core Plugin#a_gpd) | N/A         | Core   | N/A             |
| sendLoginGuestRequest     | [a_lgu](Core Plugin#a_lgu) | N/A         | Core   | N/A             |
| sendFileListRequest       | [a_gfl](Core Plugin#a_gfl) | N/A         | Core   | N/A             |
| sendServiceDetailsRequest | [a_gsd](Core Plugin#a_gsd) | N/A         | Core   | N/A             |

### Server to Client (S2C)

| Actionscript Name    | XML Tag                       | Description | Plugin | Client Response |
| -------------------- | ----------------------------- | ----------- | ------ | --------------- |
| onUserLogin          | [a_lru](Core Plugin#a_lru) | N/A         | Core   | N/A             |
| onGetServiceList     | [a_gsl](Core Plugin#a_gsl) | N/A         | Core   | N/A             |
| onGetPluginDetailes  | [a_gpd](Core Plugin#a_gpd) | N/A         | Core   | N/A             |
| onUserLogin          | [a_lgu](Core Plugin#a_lgu) | N/A         | Core   | N/A             |
| onFileListRecieve    | [a_gfl](Core Plugin#a_gfl) | N/A         | Core   | N/A             |
| onGetServiceDetailes | [a_gsd](Core Plugin#a_gsd) | N/A         | Core   | N/A             |
| onAnotherLogin       | [a_alo](Core Plugin#a_alo) | N/A         | Core   | N/A             |

## 1 - User

### Client to Server (C2S)

|Actionscript Name|XML Tag|Description|Plugin|Server Response|
|---|---|---|---|---|
|sendSaveProfileRequest|[u_sup](User Plugin#u_sup)|N/A|User|N/A|
|sendPrivateMsg|[u_spm](User Plugin#u_spm)|N/A|User|N/A|
|sendRegisterUserRequest|[u_reg](User Plugin#u_reg)|N/A|User|N/A|
|sendInvitationResponse|[u_inr](User Plugin#u_inr)|N/A|User|N/A|
|sendInvitation|[u_inv](User Plugin#u_inv)|N/A|User|N/A|
|sendGetShortProfileRquest|[u_gsp](User Plugin#u_gsp)|N/A|User|N/A|
|sendGetCountryList|[u_gwl](User Plugin#u_gwl)|N/A|User|N/A|
|sendGetFullProfileRquest|[u_gup](User Plugin#u_gup)|N/A|User|N/A|
|sendGetUserStatsRquest|[u_gus](User Plugin#u_gus)|N/A|User|N/A|
|sendGetUSAStatesList|[u_gul](User Plugin#u_gul)|N/A|User|N/A|
|sendGetFileList|[u_gfl](User Plugin#u_gfl)|N/A|User|N/A|
|sendGetCurrencyList|[u_gcl](User Plugin#u_gcl)|N/A|User|N/A|
|sendSecureQuestionRquest|[u_gsq](User Plugin#u_gsq)|N/A|User|N/A|
|sendBuddyListRequest|[u_gbl](User Plugin#u_gbl)|N/A|User|N/A|
|sendChangeFlagRequest|[u_fbd](User Plugin#u_fbd)|N/A|User|N/A|
|sendDeleteBuddyResponse|[u_dbr](User Plugin#u_dbr)|N/A|User|N/A|
|sendGetBalance|[u_gcb](User Plugin#u_gcb)|N/A|User|N/A|
|sendDeleteBuddy|[u_dbd](User Plugin#u_dbd)|N/A|User|N/A|
|sendChangePhoneStatus|[u_cph](User Plugin#u_cph)|N/A|User|N/A|
|sendChangeChatStatus|[u_ccs](User Plugin#u_ccs)|N/A|User|N/A|
|sendChangingPasswordRquest|[u_acp](User Plugin#u_acp)|N/A|User|N/A|
|sendForgottenPasswordRquest|[u_afp](User Plugin#u_afp)|N/A|User|N/A|
|sendAddBuddyResponse|[u_abr](User Plugin#u_abr)|N/A|User|N/A|
|sendAddBuddy|[u_abd](User Plugin#u_abd)|N/A|User|N/A|

### Server to Client (S2C)

|Actionscript Name|XML Tag|Description|Plugin|Client Response|
|---|---|---|---|---|
|onProfileUpdate|[u_sup](User Plugin#u_sup)|N/A|User|N/A|
|onReceivePrivateMsg|[u_spm](User Plugin#u_spm)|N/A|User|N/A|
|onUserRegistrate|[u_reg](User Plugin#u_reg)|N/A|User|N/A|
|onReceivePrivateMsg|[u_rpm](User Plugin#u_rpm)|N/A|User|N/A|
|onReceiveInvitationResponse|[u_inr](User Plugin#u_inr)|N/A|User|N/A|
|setPingTimeout|[u_p](User Plugin#u_p)|N/A|User|N/A|
|onReceiveInvitation|[u_inv](User Plugin#u_inv)|N/A|User|N/A|
|???|[u_gsp](User Plugin#u_gsp)|N/A|User|N/A|
|???|[u_gwl](User Plugin#u_gwl)|N/A|User|N/A|
|onReceiveUserProfile|[u_gup](User Plugin#u_gup)|N/A|User|N/A|
|???|[u_gus](User Plugin#u_gus)|N/A|User|N/A|
|???|[u_gul](User Plugin#u_gul)|N/A|User|N/A|
|onFileListRecieve|[u_gfl](User Plugin#u_gfl)|N/A|User|N/A|
|???|[u_gcl](User Plugin#u_gcl)|N/A|User|N/A|
|???|[u_gth](User Plugin#u_gth)|N/A|User|N/A|
|???|[u_gsq](User Plugin#u_gsq)|N/A|User|N/A|
|onReceiveBuddyList|[u_gbl](User Plugin#u_gbl)|N/A|User|N/A|
|onReceiveFlagBuddy|[u_fbd](User Plugin#u_fbd)|N/A|User|N/A|
|onReceiveDeleteBuddyRequest|[u_dbr](User Plugin#u_dbr)|N/A|User|N/A|
|???|[u_gcb](User Plugin#u_gcb)|N/A|User|N/A|
|onReceiveDeleteBuddy|[u_dbd](User Plugin#u_dbd)|N/A|User|N/A|
|onReceiveChangePhoneStatus|[u_cph](User Plugin#u_cph)|N/A|User|N/A|
|onReceiveChatStatusBuddy|[u_ccs](User Plugin#u_ccs)|N/A|User|N/A|
|onReceiveOnlineStatusBuddy|[u_cos](User Plugin#u_cos)|N/A|User|N/A|
|onReceiveChangingPassword|[u_acp](User Plugin#u_acp)|N/A|User|N/A|
|???|[u_afp](User Plugin#u_afp)|N/A|User|N/A|
|onReceiveAddBuddyRequest|[u_abr](User Plugin#u_abr)|N/A|User|N/A|
|onReceiveAddBuddy|[u_abd](User Plugin#u_abd)|N/A|User|N/A|

## 2 - Chat

### Client to Server (C2S)

|Actionscript Name|XML Tag|Description|Plugin|Server Response|
|---|---|---|---|---|
|sendEvent|[se](Chat Plugin#se)|N/A|Chat|N/A|
|sendPlayerLocation|[pl](Chat Plugin#pl)|N/A|Chat|N/A|
|onOpenDoor|[od](Chat Plugin#od)|N/A|Chat|N/A|
|onPlayerMove|[mv](Chat Plugin#mv)|N/A|Chat|N/A|
|sendChatMsg|[ms](Chat Plugin#ms)|N/A|Multiplayer, Chat|N/A|
|sendKickOutFromCrib|[ko](Chat Plugin#ko)|N/A|Chat|N/A|
|sendJoin (Multiplayer), sendJoinRoom (Chat), SEND_JoinGame (Fight), SEND_JoinGameRTT (Fight)|[jn](Chat Plugin#jn)|N/A|Multiplayer, Chat, Fight|N/A|
|onItemActivate|[ia](Chat Plugin#ia)|N/A|Chat|N/A|
|sendCreateRoom|[cr](Chat Plugin#cr)|N/A|Chat|N/A|
|sendChangeProperties|[cp](Chat Plugin#cp)|N/A|Chat|N/A|
|onPutItem|[pi](Chat Plugin#pi)|N/A|Chat|N/A|
|onRemoveItem|[ri](Chat Plugin#ri)|N/A|Chat|N/A|

### Server to Client (S2C)

| Actionscript Name           | XML Tag                    | Description                                                                                                                               | Plugin                   | Client Response |
| --------------------------- | -------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ------------------------ | --------------- |
| onReceiveSpecialEvent       | [se](Chat Plugin#se) | N/A                                                                                                                                       | Chat                     | N/A             |
| N/A                         | [pl](Chat Plugin#pl) | Receive player location                                                                                                                   | Chat                     | N/A             |
| onReceivePlayerList         | [pj](Chat Plugin#pj) | N/A                                                                                                                                       | Chat                     | N/A             |
| onReceivePlayerRemove       | [pd](Chat Plugin#pd) | N/A                                                                                                                                       | Chat                     | N/A             |
| setPingTimeout              | [p](Chat Plugin#p)   | N/A                                                                                                                                       | Galaxy, Chat             | N/A             |
| onReceivePlayerConnected    | [on](Chat Plugin#on) | N/A                                                                                                                                       | Chat                     | N/A             |
| onReceivePlayerDisconnected | [of](Chat Plugin#of) | N/A                                                                                                                                       | Chat                     | N/A             |
| onReceiveMsg                | [ms](Chat Plugin#ms) | N/A                                                                                                                                       | Multiplayer, Chat        | N/A             |
| onReceiveKickOutPlayer      | [ko](Chat Plugin#ko) | N/A                                                                                                                                       | Chat                     | N/A             |
| onJoin, MSGHND_Join (Fight) | [jn](Chat Plugin#jn) | N/A                                                                                                                                       | Multiplayer, Chat, Fight | N/A             |
| onReceiveCreateRoom         | [cr](Chat Plugin#cr) | N/A                                                                                                                                       | Chat                     | N/A             |
| onReceivePlayerProperties   | [cp](Chat Plugin#cp) | N/A                                                                                                                                       | Chat                     | N/A             |
| onReceiveCreatorLeaveCrib   | [cd](Chat Plugin#cd) | N/A                                                                                                                                       | Chat                     | N/A             |
| N/A                         | [pi](Chat Plugin#pi) | Player's turn ends because they didn't make a make before the timer ended (Mahjongg), Calls "putItemForChat" on the current screen (Chat) | Mahjongg, Chat           | N/A             |
| N/A                         | [ri](Chat Plugin#ri) | Calls "removeItemForChat" on the current screen                                                                                           | Chat                     | N/A             |

## 3 - Boxing

### Client to Server (C2S)

|Actionscript Name|XML Tag|Description|Plugin|Server Response|
|---|---|---|---|---|
|sendAction|[pe](Boxing Plugin#pe)|N/A|Boxing|N/A|

### Server to Client (S2C)

|Actionscript Name|XML Tag|Description|Plugin|Client Response|
|---|---|---|---|---|
|serverSaidChangeScore (Player) (Soccer), setPlayersScore (Player) (Pool)|[ps](Boxing Plugin#ps)|N/A|Soccer, Boxing, Pool|N/A|
|N/A|[pe](Boxing Plugin#pe)|Receives player action and pushes it to stack|Boxing|N/A|
|serverPlayAgain (Soccer)|[pa](Boxing Plugin#pa)|Play again|Soccer, Mahjongg, Boxing, Pool, Chinese Checkers|N/A|
|serverSaidChangeScore (Opponent) (Soccer), setPlayersScore (Opponent) (Pool)|[os](Boxing Plugin#os)|N/A|Soccer, Boxing|N/A|
|N/A|[oe](Boxing Plugin#oe)|Receives opponent action and pushes it to stack|Boxing|N/A|
|startNewRound (Soccer), newMPRound (Boxing)|[nr](Boxing Plugin#nr)|N/A|Soccer, Boxing|N/A|

## 4 - Mahjongg

### Client to Server (C2S)

|Actionscript Name|XML Tag|Description|Plugin|Server Response|
|---|---|---|---|---|

### Server to Client (S2C)

|Actionscript Name|XML Tag|Description|Plugin|Client Response|
|---|---|---|---|---|
|N/A|[ts](Mahjongg Plugin#ts)|N/A|Mahjongg|N/A|
|N/A|[tr](Mahjongg Plugin#tr)|Removes a pair of tiles|Mahjongg|N/A|
|N/A|[pt](Mahjongg Plugin#pt)|Player's turn|Mahjongg|N/A|
|serverPlayAgain (Soccer)|[pa](Mahjongg Plugin#pa)|Play again|Soccer, Mahjongg, Boxing, Pool, Chinese Checkers|N/A|
|N/A|[ot](Mahjongg Plugin#ot)|Opponent's turn|Mahjongg|N/A|
|N/A|[oi](Mahjongg Plugin#oi)|Opponent's turn ends because they didn't make a make before the timer ended|Mahjongg|N/A|
|N/A|[fr](Mahjongg Plugin#fr)|Freeze the game for `t` milliseconds(?)|Mahjongg|N/A|
|N/A|[pi](Mahjongg Plugin#pi)|Player's turn ends because they didn't make a make before the timer ended (Mahjongg), Calls "putItemForChat" on the current screen (Chat)|Mahjongg, Chat|N/A|

## 5 - Soccer

### Client to Server (C2S)

| Actionscript Name                                             | XML Tag                    | Description | Plugin         | Server Response |
| ------------------------------------------------------------- | -------------------------- | ----------- | -------------- | --------------- |
| sendSaveProfileRequest (Galaxy), sendStrikeParameter (Soccer) | [sp](Soccer Plugin#sp) | N/A         | Galaxy, Soccer | N/A             |
| sendMoving                                                    | [cm](Soccer Plugin#cm) | N/A         | Soccer         | N/A             |
| sendBallSave                                                  | [bs](Soccer Plugin#bs) | N/A         | Soccer         | N/A             |
| sendCharacterChosen                                           | [cc](Soccer Plugin#cc) | N/A         | Soccer         | N/A             |

### Server to Client (S2C)

|Actionscript Name|XML Tag|Description|Plugin|Client Response|
|---|---|---|---|---|
|serverSaidChangeScore (Player) (Soccer), setPlayersScore (Player) (Pool)|[ps](Soccer Plugin#ps)|N/A|Soccer, Boxing, Pool|N/A|
|serverPlayAgain (Soccer)|[pa](Soccer Plugin#pa)|Play again|Soccer, Mahjongg, Boxing, Pool, Chinese Checkers|N/A|
|serverSaidChangeScore (Opponent) (Soccer), setPlayersScore (Opponent) (Pool)|[os](Soccer Plugin#os)|N/A|Soccer, Boxing|N/A|
|startNewRound (Soccer), newMPRound (Boxing)|[nr](Soccer Plugin#nr)|N/A|Soccer, Boxing|N/A|
|parseSelectedOpponent|[oc](Soccer Plugin#oc)|N/A|Soccer|N/A|
|serverMoving|[cm](Soccer Plugin#cm)|N/A|Soccer|N/A|
|N/A|[bs](Soccer Plugin#bs)|Receive ball state|Soccer|N/A|
|parseSelected|[cc](Soccer Plugin#cc)|N/A|Soccer|N/A|

## 6 - Pool

### Client to Server (C2S)

|Actionscript Name|XML Tag|Description|Plugin|Server Response|
|---|---|---|---|---|

### Server to Client (S2C)

|Actionscript Name|XML Tag|Description|Plugin|Client Response|
|---|---|---|---|---|
|onReceiveSaveProfile (Galaxy), SetPartnerHit (Pool)|[sp](Pool Plugin#sp)|N/A|Galaxy, Pool|N/A|
|serverSaidChangeScore (Player) (Soccer), setPlayersScore (Player) (Pool)|[ps](Pool Plugin#ps)|N/A|Soccer, Boxing, Pool|N/A|
|setChosenPocket|[pc](Pool Plugin#pc)|N/A|Pool|N/A|
|serverPlayAgain (Soccer)|[pa](Pool Plugin#pa)|Play again|Soccer, Mahjongg, Boxing, Pool, Chinese Checkers|N/A|
|setStepRight (Pool), receiveTurnNotification (Chinese Checkers)|[nt](Pool Plugin#nt)|N/A|Pool, Chinese Checkers|N/A|
|preRollUpdate|[cs](Pool Plugin#cs)|N/A|Pool|N/A|

## 7 - Galaxy

### Client to Server (C2S)

| Actionscript Name                                             | XML Tag                      | Description | Plugin         | Server Response |
| ------------------------------------------------------------- | ---------------------------- | ----------- | -------------- | --------------- |
| sendStatisticVersionRequest                                   | [vsu](Galaxy Plugin#vsu) | N/A         | Galaxy         | N/A             |
| sendSaveProfileRequest (Galaxy), sendStrikeParameter (Soccer) | [sp](Galaxy Plugin#sp)   | N/A         | Galaxy, Soccer | N/A             |
| sendSaveProfilePartRequest                                    | [spp](Galaxy Plugin#spp) | N/A         | Galaxy         | N/A             |
| sendProfileVersionRequest                                     | [lpv](Galaxy Plugin#lpv) | N/A         | Galaxy         | N/A             |
| sendLoadProfileRequest                                        | [lp](Galaxy Plugin#lp)   | N/A         | Galaxy         | N/A             |
| sendGetLeaderboardStatisticRequest                            | [gls](Galaxy Plugin#gls) | N/A         | Galaxy         | N/A             |

### Server to Client (S2C)

|Actionscript Name|XML Tag|Description|Plugin|Client Response|
|---|---|---|---|---|
|onReceiveStatisticVersion|[vsu](Galaxy Plugin#vsu)|N/A|Galaxy|N/A|
|onReceiveSaveProfile (Galaxy), SetPartnerHit (Pool)|[sp](Galaxy Plugin#sp)|N/A|Galaxy, Pool|N/A|
|onReceiveResults|[rr](Galaxy Plugin#rr)|N/A|Galaxy|N/A|
|onReceiveLoadProfile|[profile](Galaxy Plugin#profile)|N/A|Galaxy|N/A|
|setPingTimeout|[p](Galaxy Plugin#p)|N/A|Galaxy, Chat|N/A|
|onReceiveProfileVersion|[lpv](Galaxy Plugin#lpv)|N/A|Galaxy|N/A|
|onReceiveLeaderboardStatistics|[gls](Galaxy Plugin#gls)|N/A|Galaxy|N/A|
|onReceiveGalaxyError|[ge](Galaxy Plugin#ge)|N/A|Galaxy|N/A|

## 8 - Fight

### Client to Server (C2S)

| Actionscript Name                                                                            | XML Tag                        | Description | Plugin                   | Server Response |
| -------------------------------------------------------------------------------------------- | ------------------------------ | ----------- | ------------------------ | --------------- |
| SEND_Punch                                                                                   | [_pu](Fight Plugin#_pu)   | N/A         | Fight                    | N/A             |
| SEND_Move                                                                                    | [_mv](Fight Plugin#_mv)   | N/A         | Fight                    | N/A             |
| SEND_Stop                                                                                    | [_st](Fight Plugin#_st)   | N/A         | Fight                    | N/A             |
| SEND_SoftReconciliation                                                                      | [_sr](Fight Plugin#_sr)   | N/A         | Fight                    | N/A             |
| SEND_Score                                                                                   | [_scr](Fight Plugin#_scr) | N/A         | Fight                    | N/A             |
| SEND_SpecialAction                                                                           | [_sa](Fight Plugin#_sa)   | N/A         | Fight                    | N/A             |
| SEND_Hit                                                                                     | [_ht](Fight Plugin#_ht)   | N/A         | Fight                    | N/A             |
| SEND_Jump                                                                                    | [_jm](Fight Plugin#_jm)   | N/A         | Fight                    | N/A             |
| SEND_Kick                                                                                    | [_ki](Fight Plugin#_ki)   | N/A         | Fight                    | N/A             |
| SEND_ExtendedPunch                                                                           | [_ep](Fight Plugin#_ep)   | N/A         | Fight                    | N/A             |
| SEND_JumpKick                                                                                | [_jk](Fight Plugin#_jk)   | N/A         | Fight                    | N/A             |
| SEND_HealthReduction                                                                         | [_hr](Fight Plugin#_hr)   | N/A         | Fight                    | N/A             |
| SEND_HeadButt                                                                                | [_hb](Fight Plugin#_hb)   | N/A         | Fight                    | N/A             |
| SEND_Unblock                                                                                 | [ul](Fight Plugin#ul)     | N/A         | Fight                    | N/A             |
| SEND_RTT                                                                                     | [rtt](Fight Plugin#rtt)   | N/A         | Fight                    | N/A             |
| SEND_Ping                                                                                    | [ping](Fight Plugin#ping) | N/A         | Fight                    | N/A             |
| sendJoin (Multiplayer), sendJoinRoom (Chat), SEND_JoinGame (Fight), SEND_JoinGameRTT (Fight) | [jn](Fight Plugin#jn)     | N/A         | Multiplayer, Chat, Fight | N/A             |
| SEND_Block                                                                                   | [bl](Fight Plugin#bl)     | N/A         | Fight                    | N/A             |

### Server to Client (S2C)

|Actionscript Name|XML Tag|Description|Plugin|Client Response|
|---|---|---|---|---|
|MSGHND_Punch|[_pu](Fight Plugin#_pu)|N/A|Fight|N/A|
|MSGHND_Move|[_mv](Fight Plugin#_mv)|N/A|Fight|N/A|
|MSGHND_Stop|[_st](Fight Plugin#_st)|N/A|Fight|N/A|
|MSGHND_SoftReconciliation|[_sr](Fight Plugin#_sr)|N/A|Fight|N/A|
|N/A|[_scr](Fight Plugin#_scr)|Set opponent score|Fight|N/A|
|MSGHND_SpecialAction|[_sa](Fight Plugin#_sa)|N/A|Fight|N/A|
|MSGHND_Hit|[_ht](Fight Plugin#_ht)|N/A|Fight|N/A|
|MSGHND_Jump|[_jm](Fight Plugin#_jm)|N/A|Fight|N/A|
|MSGHND_Kick|[_ki](Fight Plugin#_ki)|N/A|Fight|N/A|
|MSGHND_ExtendedPunch|[_ep](Fight Plugin#_ep)|N/A|Fight|N/A|
|MSGHND_JumpKick|[_jk](Fight Plugin#_jk)|N/A|Fight|N/A|
|MSGHND_HealthReduction|[_hr](Fight Plugin#_hr)|N/A|Fight|N/A|
|MSGHND_HeadButt|[_hb](Fight Plugin#_hb)|N/A|Fight|N/A|
|MSGHND_Unblock|[ul](Fight Plugin#ul)|N/A|Fight|N/A|
|MSGHND_ActionAllowance|[rpd](Fight Plugin#rpd)|N/A|Fight|N/A|
|MSGHND_ActionAllowance|[rpa](Fight Plugin#rpa)|N/A|Fight|N/A|
|MSGHND_ActionAllowance|[rka](Fight Plugin#rka)|N/A|Fight|N/A|
|MSGHND_RoundOver|[ro](Fight Plugin#ro)|N/A|Fight|N/A|
|MSGHND_ActionAllowance|[rkd](Fight Plugin#rkd)|N/A|Fight|N/A|
|MSGHND_Ping|[ping](Fight Plugin#ping)|N/A|Fight|N/A|
|N/A|[lv](Fight Plugin#lv)|N/A|Fight|N/A|
|onJoin, MSGHND_Join (Fight)|[jn](Fight Plugin#jn)|N/A|Multiplayer, Chat, Fight|N/A|
|gameOver (Multiplayer)|[go](Fight Plugin#go)|N/A|Multiplayer, Fight|N/A|
|MSGHND_ActionAllowance|[epd](Fight Plugin#epd)|N/A|Fight|N/A|
|MSGHND_ActionAllowance|[epa](Fight Plugin#epa)|N/A|Fight|N/A|
|MSGHND_Block|[bl](Fight Plugin#bl)|N/A|Fight|N/A|
|MSGHND_ActionAllowance|[akd](Fight Plugin#akd)|N/A|Fight|N/A|
|MSGHND_ActionAllowance|[aka](Fight Plugin#aka)|N/A|Fight|N/A|

## 9 - Chinese Checkers

### Client to Server (C2S)

|Actionscript Name|XML Tag|Description|Plugin|Server Response|
|---|---|---|---|---|

### Server to Client (S2C)

| Actionscript Name                                               | XML Tag                    | Description | Plugin                                           | Client Response |
| --------------------------------------------------------------- | -------------------------- | ----------- | ------------------------------------------------ | --------------- |
| serverPlayAgain (Soccer)                                        | [pa](Chinese Checkers Plugin#pa) | Play again  | Soccer, Mahjongg, Boxing, Pool, Chinese Checkers | N/A             |
| setStepRight (Pool), receiveTurnNotification (Chinese Checkers) | [nt](Chinese Checkers Plugin#nt) | N/A         | Pool, Chinese Checkers                           | N/A             |
| receiveMovement                                                 | [mv](Chinese Checkers Plugin#mv) | N/A         | Chinese Checkers                                 | N/A             |

## 10 - Trunk

### Client to Server (C2S)

|Actionscript Name|XML Tag|Description|Plugin|Server Response|
|---|---|---|---|---|
|sendTransactionsRequest|[gut](Trunk Plugin#gut)|N/A|Trunk|N/A|
|sendTransactionsCountRequest|[gutc](Trunk Plugin#gutc)|N/A|Trunk|N/A|
|sendGetUserAssetRequest|[gua](Trunk Plugin#gua)|N/A|Trunk|N/A|
|sendSplashListRequest|[gsl](Trunk Plugin#gsl)|N/A|Trunk|N/A|
|sendMoodsRequest|[gml](Trunk Plugin#gml)|N/A|Trunk|N/A|
|sendRoomsRequest|[grl](Trunk Plugin#grl)|N/A|Trunk|N/A|
|sendLootBalanceRequest|[glb](Trunk Plugin#glb)|N/A|Trunk|N/A|
|sendJammersRequest|[gjl](Trunk Plugin#gjl)|N/A|Trunk|N/A|
|sendItemsRequest|[gil](Trunk Plugin#gil)|N/A|Trunk|N/A|
|sendFamiliarsRequest|[gfl](Trunk Plugin#gfl)|N/A|Trunk|N/A|
|sendCleaningsRequest|[gcl](Trunk Plugin#gcl)|N/A|Trunk|N/A|
|sendBuyRoom|[br](Trunk Plugin#br)|N/A|Trunk|N/A|
|sendBuyMood|[bm](Trunk Plugin#bm)|N/A|Trunk|N/A|
|sendBuyItem|[bi](Trunk Plugin#bi)|N/A|Trunk|N/A|
|sendBuyJammer|[bj](Trunk Plugin#bj)|N/A|Trunk|N/A|
|sendBuyFamiliar|[bf](Trunk Plugin#bf)|N/A|Trunk|N/A|
|sendBuyCleaning|[bc](Trunk Plugin#bc)|N/A|Trunk|N/A|
|sendAssetParam|[asp](Trunk Plugin#asp)|N/A|Trunk|N/A|

### Server to Client (S2C)

|Actionscript Name|XML Tag|Description|Plugin|Client Response|
|---|---|---|---|---|
|onReceiveTransactionError|[te](Trunk Plugin#te)|N/A|Trunk|N/A|
|onReceiveUserTransactions|[gut](Trunk Plugin#gut)|N/A|Trunk|N/A|
|onReceiveUserTransactionsCount|[gutc](Trunk Plugin#gutc)|N/A|Trunk|N/A|
|onReceiveUserAsset|[gua](Trunk Plugin#gua)|N/A|Trunk|N/A|
|onReceiveSplashList|[gsl](Trunk Plugin#gsl)|N/A|Trunk|N/A|
|onReceiveMoodsList|[gml](Trunk Plugin#gml)|N/A|Trunk|N/A|
|onReceiveRoomsList|[grl](Trunk Plugin#grl)|N/A|Trunk|N/A|
|onReceiveLootBalance|[glb](Trunk Plugin#glb)|N/A|Trunk|N/A|
|onReceiveJammersList|[gjl](Trunk Plugin#gjl)|N/A|Trunk|N/A|
|onReceiveItemsList|[gil](Trunk Plugin#gil)|N/A|Trunk|N/A|
|onReceiveFamiliarsList|[gfl](Trunk Plugin#gfl)|N/A|Trunk|N/A|
|onReceiveCleaningsList|[gcl](Trunk Plugin#gcl)|N/A|Trunk|N/A|
|onReceiveBuyRoom|[br](Trunk Plugin#br)|N/A|Trunk|N/A|
|onReceiveBuyMood|[bm](Trunk Plugin#bm)|N/A|Trunk|N/A|
|onReceiveBuyItem|[bi](Trunk Plugin#bi)|N/A|Trunk|N/A|
|onReceiveBuyJammer|[bj](Trunk Plugin#bj)|N/A|Trunk|N/A|
|onReceiveBuyFamiliar|[bf](Trunk Plugin#bf)|N/A|Trunk|N/A|
|onReceiveBuyCleaning|[bc](Trunk Plugin#bc)|N/A|Trunk|N/A|

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
