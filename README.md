# API suggested specs

These are JSON-like specs for the data we expect to receive.

JSON properties are written in the following format: `"key" [quantifier]: valueType`.

- `"key"`: literal key name, lowercaseCamelCase
- `quantifier`:
  - [absence]: property is **obligatory**
  - `*`: 0 or more array items; property is optional
  - `+`: 1 or more array items; property is **obligatory**
  - `?`: 0 or 1; property is optional
  - `{n}`: exactly _n_ ocurrences; property is **obligatory**
- `valueType`:
  - `UppercaseCamelCase`: data type
  - `lowercase_snake_case`: String format


## Fairphone

### Angels endpoint

```JavaScript
{
  "angels" *: [
    {
      "cityName": String,
      "countryName" ?: String,
      "coordinates": {
        "latitude": Float,
        "longitude": Float
      },
      "email": email,
      "people" *: [
        {
          "name" ?: String,
          "forumNick" ?: String
        },
        {...}
      ]
    },
    {...}
  ]
}
```


### Meetups endpoint

```JavaScript
{
  "meetups" *: [
    {
      "eventName": String,
      "startDate": date,
      "endDate": date,
      "address" ?: String,
      "coordinates": {
        "latitude": Float,
        "longitude": Float
      },
      "website": url
    },
    {...}
  ]
}
```

- `address`: readable address for showing it to the user.

- `date`: formated as UNIX time (seconds since the Epoch) or ISO-8601. Examples: `1474505000`, `2016-09-22T17:45:37Z`, `2016-09-22` (only date).


## T-Mobile

### Shops endpoint
```JavaScript
{
  "shops" *: [
    {
      "shopName": String,
      "shopAddress" ?: String,
      "coordinates": {
        "latitude": Float,
        "longitude": Float
      },
      "openingHours" {7}: [ // Starts on monday
        {
          "openingTime": time,
          "closingTime": time
        },
        {...}
      ],
      "website" ?: url,
      "phoneNumber" ?: phone_number
    },
    {...}
  ]
}
```

- `shopAddress`: readable address for showing it to the user.

- `time`: language-agnostic 24-hours value with minutes. Examples: `9:15`, `20.00`. Avoid: `19hrs`.
- `phone_number`: phone number for showing it to the user. Only numbers and spaces. Avoid special characters. Example: `0676 123 45 67`.
