# Lobby Examples

## Guest Human Player

1. main page (From AuthController)
1. (client to server) select a village list; [enterLobbyForHumanPlayer.json](https://werewolf.world/example/0.2/enterLobbyForHumanPlayer.json)
1. (server to client) go to a page of a village list; [lobbyForHumanPlayer.json](https://werewolf.world/example/0.2/lobbyForHumanPlayer.json)
1. (client to server) select a village; [selectVillageForHumanPlayer.json](https://werewolf.world/example/0.2/selectVillageForHumanPlayer.json)
1. (server to client) go to a waiting page; [waitingPageForHumanPlayer.json](https://werewolf.world/example/0.2/waitingPageForHumanPlayer.json)
1. a host player pushes a start button (To GameController)

(client to server) leave a waiting page [leaveWaitingPage.json](https://werewolf.world/example/0.2/leaveWaitingPage.json)

## Host Human Player

1. main page (From AuthController)
1. (client to server) select a village list; [enterLobbyForHumanPlayer.json](https://werewolf.world/example/0.2/enterLobbyForHumanPlayer.json)
1. (server to client) go to a page of a village list; [lobbyForHumanPlayer.json](https://werewolf.world/example/0.2/lobbyForHumanPlayer.json)
1. (client) push a button for building a village
1. (client) go to a page for building a village
1. (client to server) build a village; [buildVillage.json](https://werewolf.world/example/0.2/buildVillage.json)
1. (server to client) go to a waiting page; [waitingPageForHumanPlayer.json](https://werewolf.world/example/0.2/waitingPageForHumanPlayer.json)
1. a host player pushes a start button (To GameController)

(client to server) leave a waiting page [leaveWaitingPage.json](https://werewolf.world/example/0.2/leaveWaitingPage.json)  
Then, a host of a waiting page is selected from remaining players if they exist.

(client to server) kick out a player [kickOutPlayer.json](https://werewolf.world/example/0.2/kickOutPlayer.json)  
The kicked out player moves to a lobby with an error message that a host kicked out the player