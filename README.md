#### Trello Board

[Trello board](https://trello.com/b/Hxn9cz4r/q3-spotify)

#### WireFrames

[Wireframes](https://www.lucidchart.com/documents/edit/c8b77119-9795-4ad6-8da5-13fe8cc622c5/0?shared=true&)

#### Style Guide

[style guide](styleGuideSpotifyRew.jpg)

#### ERD

[ERD](https://www.lucidchart.com/documents/edit/040a2f7a-7baf-421a-84f4-c07f5d26a816/0)

#### Route Plan
##### auth
get /auth/spotify/callback --> redirect user to webpage with query strings attached including api tokens also adds new users to database/updates user info

get /auth/spotify --> redirect user to spotify OAuth

##### user
get /api/users/:uid --> gets user info from database

##### playlists
get /api/users/:uid/playlists --> gets all user playlists

post /api/users/:uid/playlists --> posts a playlist

get /api/users/:uid/playlists/:pid --> gets specific playlist from user

patch /api/users/:uid/playlists/:pid --> edit a playlist

delete /api/users/:uid/playlists/:pid --> delete a playlist --> also deletes all versions of that playlist

##### playlist versions
get /api/users/:uid/playlists/:pid/versions --> gets all versions of a users playlist

post /api/users/:uid/playlists/:pid/versions --> create a new version of a users playlist

get /api/users/:uid/playlists/:pid/versions/:vid --> gets specific version of a users playlist --> spits out track list

delete /api/users/:uid/playlists/:pid/versions/:vid --> delete a version of a playlist

##### tracks
get /api/tracks/:id --> get track info
