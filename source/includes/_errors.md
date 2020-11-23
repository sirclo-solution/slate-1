# Errors

The API uses the following error codes:

| Error Code | Meaning                                                                                   |
| ---------- | ----------------------------------------------------------------------------------------- |
| 400        | Bad Request -- Your request is invalid                                                    |
| 401        | Unauthorized -- Your API key is wrong.                                                    |
| 403        | Forbidden -- The Order and Product requested is hidden for administrators only.           |
| 404        | Not Found -- The specified Order and Product could not be found.                          |
| 500        | Internal Server Error -- We had a problem with our server. Try again later.               |
| 503        | Service Unavailable -- We're temporarily offline for maintenance. Please try again later. |
