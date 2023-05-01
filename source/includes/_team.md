# Teams

## Upload team data

```shell
curl --location 'http://api.replay.dk/Teams' \
--header 'Authorization: your_jwt_token' \
--form 'file=@"/path/to/file"'
```

> The above command returns JSON structured like this:

```json
{
  "message": "Successfully added!"
}
```

This endpoint uploads team data to the backend.

### HTTP Request

`POST http://api.replay.dk/Teams`

### URL Parameters

| Parameter | in           | Default | Description                                        |
| --------- | ------------ | ------- | -------------------------------------------------- |
| file      | request body | NULL    | the playlist zip file to be uploaded on the bucket |

## Get team data

```shell
curl --location 'http://api.replay.dk/Teams/:<TeamId>' \
--header 'Authorization: your_jwt_token'
```

> The above command returns JSON structured like this:

```json
{
  "uuid": "6d3b6d7c-24f1-4e1b-99e6-2e218837c39e",
  "name": "AC Horsens",
  "short_name": "ACH",
  "league_name": "",
  "country": "",
  "asset_bundle": ""
}
```

This endpoint gets team data from the backend.

### HTTP Request

`GET http://api.replay.dk/Teams/<TeamId>`

### URL Parameters

| Parameter | in           | Default | Description                                        |
| --------- | ------------ | ------- | -------------------------------------------------- |
| file      | request body | NULL    | the playlist zip file to be uploaded on the bucket |
