# Players

## Upload player data

```shell
curl --location 'http://api.replay.dk/Players' \
--header 'Authorization: your_jwt_token' \
--form 'file=@"/path/to/file"'
```

> The above command returns JSON structured like this:

```json
{
  "message": "Successfully added!"
}
```

This endpoint uploads player data to the backend.

### HTTP Request

`POST http://api.replay.dk/Players`

### URL Parameters

| Parameter | in           | Default | Description                                        |
| --------- | ------------ | ------- | -------------------------------------------------- |
| file      | request body | NULL    | the playlist zip file to be uploaded on the bucket |

## Get team data

```shell
curl --location 'http://api.replay.dk/Players/:<PlayerId>' \
--header 'Authorization: your_jwt_token'
```

> The above command returns JSON structured like this:

```json
{
  "uuid": "27ea4401-fc10-4a63-938f-272efefce213",
  "team_uuid": "6d3b6d7c-24f1-4e1b-99e6-2e218837c39e",
  "name": "L. Tim",
  "fullname": "Lars Tim",
  "jersey_number": "40",
  "assetbundle": ""
}
```

This endpoint gets players data from the backend.

### HTTP Request

`GET http://api.replay.dk/Players/<PlayerId>`

### URL Parameters

| Parameter | in           | Default | Description                                        |
| --------- | ------------ | ------- | -------------------------------------------------- |
| file      | request body | NULL    | the playlist zip file to be uploaded on the bucket |
