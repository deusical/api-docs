# API Docs

Here I'll just post some documentation on my apis...

## Nitrotype API

### https://nitrotype.deusical.workers.dev/

#### /racer/[name]

Returns info of user (make sure to supply username)

If user is valid, it will return something similar to 
```json
{
  "success": true,
  "data" {...}
}
```
with a status code of 200.
If the user is invalid, it will return 
```json
{
  "success": false,
  "data": "invalid user"
}
```
with a status code of 400

#### /team/[name]

Returns info of team

If team exists, it will return something similar to 
```json
{
  "success": true,
  "data" {...}
}
```
with a status code of 200.
If the team doesn't exist, it will return
```json
{
    "success": false,
    "data": {
        "noTeam": true
    }
}
```
with a status code of 400

#### /leaderboards/[racers:season, racers:daily, teams:season, teams:daily]

This will return info of current leaderboards.
You need to specify one of the options above or else it won't return anything.
Example: https://nitrotype.deusical.workers.dev/leaderboards/teams:season

It'll return data similar to this:
```json
{
  "success": true,
  "data" {...}
}
```
with a status code of 200.
If any errors happen, it'll return with a status code of 400.
