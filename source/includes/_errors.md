# Errors

The Wellthie Individual (INDV) API uses the following error codes:

Error Code | Meaning
---------- | -------
400 | Bad Request -- Your request is invalid.
401 | Unauthorized -- Your credentials are wrong or you are not authorized to access the requested data.
403 | Forbidden -- The user isn't authorized to access the requested data.
404 | Not Found -- The requested data could not be found.
406 | Not Acceptable -- You requested a format that isn't json.
429 | Too Many Requests -- We see a lot of requests from your end! Slow down!
500 | Internal Server Error -- We had a problem with our server. Try again later.
503 | Service Unavailable -- We're temporarily offline for maintenance. Please try again later.
