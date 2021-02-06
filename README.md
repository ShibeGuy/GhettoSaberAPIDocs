# GhettoSaber API Documentation

Hello. If you are here you are either stalking my GitHub or you saw the ping in discord.


# Endpoints

All endpoints are accessible from /api.
# Misc Endpoints
## GET /copypasta

Returns all of the copypastas stored.

## GET /news/[hash]
Returns all news objects, sorted by latest. Optional hash gets a specific article by its hash. 

# Rank Related Endpoints
##  GET /ranks/global/[page]
Gets global rankings. Optional page offsets it by 50.
## GET /ranks/global/search/<playername\>
Gets a list of players with similar names to search, ordered by rank. 
## GET /ranks/country/<2LetterCountryCode>/[page]
Gets a countries rankings by their code. Optional page offsets it by 50.
# User Related endpoints
## GET /users/<hash\>/[full|basic]
Gets a user's profile using their hash. Optional full or basic will show the full profile or the basic profile respectively. 
## GET /users/by-name/<name\>/[full|basic]
Gets a user's profile using their username. Optional full or basic will show the full profile or the basic profile respectively. 
## GET /users/by-id/<id\>
Get's a user using their steam/oculus id. This is for easier compatibility with ScoreSaber and HitBloq. 

# Song Leaderboard Related Endpoints
I am too tired to document these right now, have fun making sense of my express.js code
```js
app.get('/api/leaderboards/id/*/difficulty/*', endpoints.leaderboardIdDifficulty);

app.get('/api/leaderboards/id/*/difficulty/*/characteristic/*', endpoints.leaderboardIdDifficultyCharacteristic);

app.get('/api/leaderboards/hash/*/difficulty/*', endpoints.leaderboardHashDifficulty);

app.get('/api/leaderboards/hash/*/difficulty/*/characteristic/*', endpoints.leaderboardHashDifficultyCharacteristic);

app.get('/api/leaderboards/ranked', endpoints.leaderboardRanked);
```
# Ranking Related Endpoints
## GET /ranking/queue
Returns an array of all the ranking requests, regardless of status.
## GET /ranking/request/<hash\>
Gets a specific ranking request using its hash.
