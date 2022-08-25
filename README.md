# Music-API-Docs

### Get a specific artist's details based on artistId

Request components:

- Method:"GET"
- URL:('/artists/:artistId)
- Headers:none
- Body:none

Response components:

- Status code:200
- Headers:('content-type','application/json)
- Body:{
    "name": "Red Hot Chili Peppers",
    "artistId": 1,
    "albums": [
        {
            "name": "Stadium Arcadium",
            "albumId": 1,
            "artistId": 1
        }
    ]
}

### Add an artist

Request components:

- Method:'POST'
- URL:/artists
- Headers:('content-type','application/json)
- Body: {
    artistId:true,
    name:true
}

Response components:

- Status code:201
- Headers:('content-type','application/json)
- Body:{
    "name": "Foo Figthers",
    "artistId": 2
}

### Edit a specified artist by artistId

Request components:

- Method:'PUT'
- URL:/artists/:artistId
- Headers:('content-type','application/json)
- Body:{
    artistId:true,
    name:true
}

Response components:

- Status code:200;
- Headers:('content-type','application/json)
- Body:{
    "name": "Imagine Dragons",
    "artistId": 2,
    "updatedAt": "2022-08-25T21:34:51.669Z"
}

### Delete a specified artist by artistId

Request components:

- Method:'DELETE'
- URL:/artists/:artistId
- Headers:none
- Body:none

Response components:

- Status code:200
- Headers: ('content-type','application/json)
- Body:{
    "message": "Sucessfully deleted"
}

### Get all albums of a specific artist based on artistId

Request components:

- Method:'GET'
- URL:/artists/:artistId/albums
- Headers:none
- Body:none

Response components:

- Status code:200
- Headers:('content-type','application/json)
- Body:[{"name":"Stadium Arcadium","albumId":1,"artistId":1}]

### Get a specific album's details based on albumId

Request components:

- Method:'GET'
- URL:/albums/:albumId
- Headers:none
- Body:none

Response components:

- Status code: 200
- Headers: ('content-type','application/json)
- Body: {
    "name": "Stadium Arcadium",
    "albumId": 1,
    "artistId": 1,
    "artist": {
        "name": "Red Hot Chili Peppers",
        "artistId": 1
    },
    "songs": [
        {
            "name": "Dani California",
            "lyrics": "...",
            "trackNumber": 1,
            "songId": 1,
            "createdAt": "2022-08-25T22:27:20.000Z",
            "updatedAt": "2022-08-25T22:27:20.000Z",
            "albumId": 1
        }
    ]
}

### Add an album to a specific artist based on artistId

Request components:

- Method:"POST"
- URL:/artists/:artistId/albums
- Headers:('content-type','application/json)
- Body:{
    albumId: true,
    name:true,
    artistId:true
}

Response components:

- Status code:201
- Headers:('content-type','application/json)
- Body:{
    "name": "Imagine Dragons",
    "albumId": 2,
    "artistId": 1
}

### Edit a specified album by albumId

Request components:

- Method:"PUT"
- URL:/albums/:albumId
- Headers:('content-type','application/json)
- Body:{
    "name": "starlight",
    "albumId": 2,
    "artistId": 1
}

Response components:

- Status code:200
- Headers:('content-type','application/json)
- Body:{
    "name": "starlight",
    "albumId": 2,
    "artistId": 1,
    "updatedAt": "2022-08-25T22:46:43.471Z"
}

### Delete a specified album by albumId

Request components:

- Method:"DELETE"
- URL:/albums/:albumId
- Headers:none
- Body:none

Response components:

- Status code:200
- Headers:('content-type','application/json)
- Body:{
    "message": "Sucessfully deleted"
}

### Get all songs of a specific artist based on artistId

Request components:

- Method:"GET"
- URL:/artists/:artistId/songs
- Headers:none
- Body:none

Response components:

- Status code:200
- Headers:('content-type','application/json)
- Body:[
    {
        "name": "Dani California",
        "lyrics":"...",
        "trackNumber": 1,
        "songId": 1,
        "albumId": 1
    }
]

### Get all songs of a specific album based on albumId

Request components:

- Method:"GET"
- URL:/albums/:albumId/songs
- Headers:none
- Body:none

Response components:

- Status code:200
- Headers:('content-type','application/json)
- Body:[
    {
        "name": "Dani California",
        "lyrics":"...",
        "trackNumber": 1,
        "songId": 1,
        "albumId": 1
    }
]




### Get all songs of a specified trackNumber
Request components:

- Method:"GET"
- URL:/songs/:trackNumber
- Headers:none
- Body:none

Response components:

- Status code: 200
- Headers: ('content-type','application/json)
- Body:{
    "name": "Dani California",
    "lyrics": "..." ,
    "trackNumber": 1,
    "songId": 1,
    "albumId": 1,
    "album": {
        "name": "Stadium Arcadium",
        "albumId": 1,
        "artistId": 1
    },
    "artist": {
        "name": "Red Hot Chili Peppers",
        "artistId": 1
    }
}


### Get a specific song's details based on songId

Request components:

- Method:"GET"
- URL:/songs/:songId
- Headers:none
- Body:none

Response components:

- Status code: 200
- Headers: ('content-type','application/json)
- Body:{
    "name": "Dani California",
    "lyrics": "...",
    "trackNumber": 1,
    "songId": 1,
    "albumId": 1,
    "album": {
        "name": "Stadium Arcadium",
        "albumId": 1,
        "artistId": 1
    },
    "artist": {
        "name": "Red Hot Chili Peppers",
        "artistId": 1
    }
}

### Add a song to a specific album based on albumId

Request components:

- Method:"POST"
- URL:/albums/:albumId/songs
- Headers:('content-type','application/json)
- Body:{
    "name": true,
    "lyrics": true,
    "trackNumber": true,
}

Response components:

- Status code:201
- Headers: ('content-type','application/json)
- Body:{
    "name": "Imagine",
    "lyrics": "hvbcjguyefugdjhabgfkjfuyadukgfluy",
    "trackNumber": 2,
    "songId": 2,
    "albumId": 1
}

### Edit a specified song by songId

Request components:

- Method:"PUT"
- URL:/songs/:songId
- Headers: ('content-type','application/json)
- Body:Body:{
    "name": "Imagine",
    "lyrics": "1234567",
    "trackNumber": 2
}

Response components:

- Status code: 200
- Headers: ('content-type','application/json)
- Body: {
    "name": "Imagine",
    "lyrics": "1234567",
    "trackNumber": 2,
    "songId": 2,
    "albumId": 1,
    "updatedAt": "2022-08-25T23:15:35.039Z"
}

### Delete a specified song by songId

Request components:

- Method:
- URL:
- Headers:
- Body:

Response components:

- Status code:
- Headers: ('content-type','application/json)
- Body:
