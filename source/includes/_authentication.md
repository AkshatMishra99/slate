# Authentication

## Get OTP

```shell
curl --request POST "http://api.replay.dk/Auth/GetOTP" \
  -H "Content-Type: application/json"
  --data '{
    "phone": "99999999"
  }'
```

This request will trigger an OTP at the provided number.

### HTTP Request

`POST http://api.replay.dk/Auth/GetOTP`

## Resend OTP

```shell
curl --request POST "http://api.replay.dk/Auth/ResendOTP" \
  -H "Content-Type: application/json"
  --data '{
    "phone": "99999999"
  }'
```

This request will trigger an OTP at the provided number.

### HTTP Request

`POST http://api.replay.dk/Auth/ResendOTP`

## Verify OTP

```shell
curl --request POST "http://api.replay.dk/Auth/VerifyOTP" \
  -H "Content-Type: application/json"
  --data '{
    "otp": "XXXXXX",
    "phone": "99999999"
  }'
```

This request will verify the OTP at the provided number. If the OTP is verified, it will return a JWT token to authenticate further requests.

### HTTP Request

`POST http://api.replay.dk/Auth/VerifyOTP`

<aside class="notice">
You must replace <code>999999999</code> with your personal API key.
</aside>

## Authentication

```shell
curl --request GET "http://api.replay.dk/" \
  -H "Authorization: your_jwt_token"
```

For each request add your JWT token in the Authorization header for it be authenticated successfully.
