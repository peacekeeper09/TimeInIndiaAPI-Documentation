# TimeInIndiaAPI-Documentation

## Introduction

Welcome to the Time in India API! This API provides the current time in both 24-hour and 12-hour formats for the Indian timezone.

## Base URL

The base URL for this API is:

```
https://timeinindiaapi.onrender.com
```

## Get Current Time

### Endpoint

```
GET /get_time
```

This endpoint returns the current time in 24-hour and 12-hour formats.

### Request

- **Method:** `GET`
- **URL:** `https://timeinindiaapi.onrender.com/get_time`

### Response

The response will be a JSON object containing the current time in 24-hour and 12-hour formats.

```json
{
  "time_24hr_format": "00:00:25",
  "time_12hr_format": "12:00:25 AM"
}
```

## Example Usage

### cURL

```bash
curl https://timeinindiaapi.onrender.com/get_time
```

### Python (requests)

```python
import requests

url = "https://timeinindiaapi.onrender.com/get_time"
response = requests.get(url)
data = response.json()

print("Time in 24-hour format:", data["time_24hr_format"])
print("Time in 12-hour format:", data["time_12hr_format"])
```

### Javascript (requests)

```
const url = 'https://timeinindiaapi.onrender.com/get_time';

fetch(url)
  .then(response => {
    if (!response.ok) {
      throw new Error(`HTTP error! Status: ${response.status}`);
    }
    return response.json();
  })
  .then(data => {
    console.log('Time in 24-hour format:', data.time_24hr_format);
    console.log('Time in 12-hour format:', data.time_12hr_format);
  })
  .catch(error => console.error('Error:', error));
```

## Notes

- All times are provided in the Indian timezone (Asia/Kolkata).
- The API is open and does not require authentication.

Feel free to use this API to retrieve the current time in India for your applications!

---

