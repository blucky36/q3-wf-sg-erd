## Trello Board

[Trello board](https://trello.com/b/Hxn9cz4r/q3-spotify)

## WireFrames

[Wireframes](https://www.lucidchart.com/invitations/accept/ce0a0e38-ec15-470e-9044-eb91afb1c47b)

## Style Guide

[style guide](styleGuideSpotifyRew.jpg)

## ERD

[ERD](https://www.lucidchart.com/invitations/accept/4c586819-2265-43d1-841b-bfd202efe13a)

## Front End Repo

[Click Me](https://github.com/blucky36/spotify-rewind-frontend)

## Back End Repo

[Click Me](https://github.com/blucky36/Q3spotify-rewind-backend)

## Route Plan
### auth
get /auth/spotify/callback --> redirect user to webpage with query strings attached including api tokens also adds new users to database/updates user info

get /auth/spotify --> redirect user to spotify OAuth DONE

### user
get /api/users/:uid --> gets user info from database

### playlists
get /api/users/:uid/playlists --> gets all user playlists

post /api/users/:uid/playlists --> posts a playlist

get /api/users/:uid/playlists/:pid --> gets specific playlist from user DONE

patch /api/users/:uid/playlists/:pid --> edit a playlist

delete /api/users/:uid/playlists/:pid --> delete a playlist --> also deletes all versions of that playlist DONE

### playlist versions
get /api/users/:uid/playlists/:pid/versions --> gets all versions of a users playlist

post /api/users/:uid/playlists/:pid/versions --> create a new version of a users playlist

get /api/users/:uid/playlists/:pid/versions/:vid --> gets specific version of a users playlist --> spits out track list DONE

delete /api/users/:uid/playlists/:pid/versions/:vid --> delete a version of a playlist DONE

### tracks
get /api/tracks/:id --> get track info
