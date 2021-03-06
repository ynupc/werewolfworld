["@homepage": "http://werewolf.world"](http://werewolf.world)

"version": "0.1"

# Contexts

|Contexts|JSON-LD|
---|---
|base|[http://werewolf.world/context/0.1/base.jsonld](http://werewolf.world/context/0.1/base.jsonld)|
|error|[http://werewolf.world/context/0.1/error.jsonld](http://werewolf.world/context/0.1/error.jsonld)|
|agent|[http://werewolf.world/context/0.1/agent.jsonld](http://werewolf.world/context/0.1/agent.jsonld)|
|role|[http://werewolf.world/context/0.1/role.jsonld](http://werewolf.world/context/0.1/role.jsonld)|
|board|[http://werewolf.world/context/0.1/board.jsonld](http://werewolf.world/context/0.1/board.jsonld)|
|chat|[http://werewolf.world/context/0.1/chat.jsonld](http://werewolf.world/context/0.1/chat.jsonld)|
|vote|[http://werewolf.world/context/0.1/vote.jsonld](http://werewolf.world/context/0.1/vote.jsonld)|
|votingResults|[http://werewolf.world/context/0.1/votingResults.jsonld](http://werewolf.world/context/0.1/votingResults.jsonld)|
|scroll|[http://werewolf.world/context/0.1/scroll.jsonld](http://werewolf.world/context/0.1/scroll.jsonld)|

# IRIs

## message

|IRI|Purpose|
---|---
|http://werewolf.world/resource/0.1/boardMessage|Send a prediction board update to server|
|http://werewolf.world/resource/0.1/errorMessage|Send/Receive an error message to/from server|
|http://werewolf.world/resource/0.1/playerMessage|Send/receive a chat message to/from server|
|http://werewolf.world/resource/0.1/scrollMessage|Send a scroll information to server|
|http://werewolf.world/resource/0.1/systemMessage|Receive a system message from server|
|http://werewolf.world/resource/0.1/voteMessage|Send a vote to server|

## base

|IRI|Type|Values|
---|---|---
|http://werewolf.world/resource/0.1/token||(GUID)|
|http://werewolf.world/resource/0.1/villageId|xsd:integer|0 <=|
|http://werewolf.world/resource/0.1/villageName||5 <= {# of Unicode code points} <= 30|
|http://werewolf.world/resource/0.1/phase||'day conversation', 'day vote', 'night', 'results', 'post mortem'|
|http://werewolf.world/resource/0.1/date|xsd:integer|-1 <=, 0 when phase were post mortem, -1 when phase were results|
|http://werewolf.world/resource/0.1/phaseTimeLimit||'none' or such as '10m', '3m'|
|http://werewolf.world/resource/0.1/phaseStartTime|xsd:dateTime|such as '2006-10-07T12:06:56.568+09:00'|
|http://werewolf.world/resource/0.1/serverTimestamp|xsd:dateTime|such as '2006-10-07T12:06:56.568+09:00'|
|http://werewolf.world/resource/0.1/clientTimestamp|xsd:dateTime|such as '2006-10-07T12:06:56.568+09:00'|
|http://werewolf.world/resource/0.1/directionality||'server to client' or 'client to server'|
|http://werewolf.world/resource/0.1/channel||'public', 'private', 'werewolf', 'master', 'grave', 'onymousAudience', 'anonymousAudience'|


## error

|IRI|Type|Values|
---|---|---
|http://werewolf.world/resource/0.1/errorContent|||
|http://werewolf.world/resource/0.1/severity||'error', 'warning'|
|http://werewolf.world/resource/0.1/source||(JSON-LD)|

## agent

|IRI|Type|Values|
---|---|---
|http://werewolf.world/resource/0.1/agent|||
|http://werewolf.world/resource/0.1/agentId|xsd:integer|-1 <= (-1 means master)|
|http://werewolf.world/resource/0.1/agentIsMine|xsd:boolean|true, false|
|http://werewolf.world/resource/0.1/agentName||[http://werewolf.world/image/0.1/#agent](http://werewolf.world/image/0.1/#agent)|
|http://werewolf.world/resource/0.1/agentImage||[http://werewolf.world/image/0.1/#agent](http://werewolf.world/image/0.1/#agent)|
|http://werewolf.world/resource/0.1/agentStatus||'alive', 'dead', 'death by execution', 'death by werewolf attack', 'death by fear', 'unnatural death'|

See [http://werewolf.world/image/0.1/#agent](http://werewolf.world/image/0.1/#agent)

## role

|IRI|Type|Values|
---|---|---
|http://werewolf.world/resource/0.1/role|||
|http://werewolf.world/resource/0.1/roleIsMine|xsd:boolean|true, false|
|http://werewolf.world/resource/0.1/roleName||[http://werewolf.world/image/0.1/#role](http://werewolf.world/image/0.1/#role)|
|http://werewolf.world/resource/0.1/roleImage||[http://werewolf.world/image/0.1/#role](http://werewolf.world/image/0.1/#role)|
|http://werewolf.world/resource/0.1/roleNumber|xsd:integer|0 <=, <= 7|

See [http://werewolf.world/image/0.1/#role](http://werewolf.world/image/0.1/#role)

## board

|IRI|Type|Values|
---|---|---
|http://werewolf.world/resource/0.1/board|||
|http://werewolf.world/resource/0.1/boardPolarity||'positive', 'negative'|
|http://werewolf.world/resource/0.1/boardPrediction||'?','Δ','O','X'|

## chat

|IRI|Type|Values|
---|---|---
|http://werewolf.world/resource/0.1/chatIsMine|xsd:boolean|true, false|
|http://werewolf.world/resource/0.1/chatId|xsd:integer|1 <=|
|http://werewolf.world/resource/0.1/chatCounter|xsd:integer|0<=, <=chatCounter|
|http://werewolf.world/resource/0.1/chatLimit|xsd:integer|1 <=|
|http://werewolf.world/resource/0.1/chatInterval||such as '5s'|
|http://werewolf.world/resource/0.1/chatText||string such as 0 <= {# of Unicode code points} <= {chatCharacterLimit}|
|http://werewolf.world/resource/0.1/chatCharacterLimit|xsd:integer|1 <= {# of Unicode code points}|
|http://werewolf.world/resource/0.1/chatLanguage||'en', 'ja', etc. ([java.util.Locale.toString](https://docs.oracle.com/javase/9/docs/api/java/util/Locale.html#toString--))|
|http://werewolf.world/resource/0.1/chatIsOver|xsd:boolean|true, false|

## votingResults

|IRI|Type|Values|
---|---|---
|http://werewolf.world/resource/0.1/votingResultsSummary|||
|http://werewolf.world/resource/0.1/numberOfVotes|xsd:integer|0 <=, <= {number of alive agents except a master}|
|http://werewolf.world/resource/0.1/rankOfVotes|xsd:integer|1 <=, 1 is the highest. "1224" ranking.|
|http://werewolf.world/resource/0.1/votingResultsDetails|||

## result

|IRI|Type|Values|
---|---|---
|http://werewolf.world/resource/0.1/result||'win', 'lose'|
|http://werewolf.world/resource/0.1/userName||5 <= {# of Unicode code points} <= 15|
|http://werewolf.world/resource/0.1/userAvatar||(URL)|

## scroll

|IRI|Type|Values|
---|---|---
|http://werewolf.world/resource/0.1/nodeId|||
|http://werewolf.world/resource/0.1/scrollTop|xsd:integer||
|http://werewolf.world/resource/0.1/scrollHeight|xsd:integer||
|http://werewolf.world/resource/0.1/offsetHeight|xsd:integer||
