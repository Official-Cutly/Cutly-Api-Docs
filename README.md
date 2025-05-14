## API Reference

### Create a short URL

```http
POST /shorten
```

| Parameter        | Type     | Description                                |
| :--------------- | :------- | :----------------------------------------- |
| `destinationUrl` | `string` | **Required**. The long URL to be shortened |

#### Response

```json
{
  "shortUrl": "https://cutly-api.vercel.app/abc1234"
}
```

### Update the long URL associated with a short URL

```http
PUT /update
```

| Parameter        | Type     | Description                                                        |
| :--------------- | :------- | :----------------------------------------------------------------- |
| `shortUrl`       | `string` | **Required**. The short URL to be updated                          |
| `destinationUrl` | `string` | **Required**. The new long URL to be associated with the short URL |

#### Response

```json
{
  "success": true
}
```

### Redirect to the long URL associated with a short URL

```http
GET /:urlCode
```

| Parameter | Type     | Description                      |
| :-------- | :------- | :------------------------------- |
| `urlCode` | `string` | **Required**. The short URL code |

#### Response

Redirects to the long URL associated with the short URL

### Update the expiry date of a short URL

```

| Parameter   | Type     | Description                                                |
| :---------- | :------- | :--------------------------------------------------------- |
| `shortUrl`  | `string` | **Required**. The short URL to be updated                  |

#### Response

```json
{
  "success": true
}
```
