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

- Method:
- URL:
- Headers:
- Body:

Response components:

- Status code:
- Headers:
- Body:

### Edit a specified album by albumId

Request components:

- Method:
- URL:
- Headers:
- Body:

Response components:

- Status code:
- Headers:
- Body:

### Delete a specified album by albumId

Request components:

- Method:
- URL:
- Headers:
- Body:

Response components:

- Status code:
- Headers:
- Body:

### Get all songs of a specific artist based on artistId

Request components:

- Method:
- URL:
- Headers:
- Body:

Response components:

- Status code:
- Headers:
- Body:

### Get all songs of a specific album based on albumId

Request components:

- Method:
- URL:
- Headers:
- Body:

Response components:

- Status code:
- Headers:
- Body:
