Updated on 7th November, 2017

# A warm welcome to Example Docs

You are welcome to modify this file!

## Introduction

The API is organized around REST. Our API has predictable, resource-oriented URLs, and uses HTTP response codes to indicate API errors. We use built-in HTTP features, like HTTP authentication and HTTP verbs, which are understood by off-the-shelf HTTP clients. JSON is returned by all API responses, including errors, although our API libraries convert responses to appropriate language-specific objects.

## Errors

The API uses conventional HTTP response codes to indicate the success or failure of an API request. In general, codes in the `2xx` range indicate success, codes in the `4xx` range indicate an error that failed given the information provided (e.g., a required parameter was omitted, a data doesn't exist, etc.), and codes in the `5xx` range indicate an error with servers (these are rare).

Not all errors map cleanly onto HTTP response codes, however. When a request is valid but does not complete successfully (e.g., a user has reached the free plan), we return a `402` error code.

**Attributes**

|                   Name | Description                              |
| ---------------------: | ---------------------------------------- |
| message<br/>`optional` | A human-readable message providing more details about the error. Only selected errors can be shown to users. |

**HTTP status code summary**

|                        Status Code | Description                              |
| ---------------------------------: | ---------------------------------------- |
|                           200 - OK | Everything worked as expected.           |
|                  400 - Bad Request | The request was unacceptable, often due to missing a required parameter. |
|                 401 - Unauthorized | No valid API key provided.               |
|               402 - Request Failed | The parameters were valid but the request failed. |
|                    404 - Not Found | The requested resource doesn't exist.    |
|                     409 - Conflict | The request conflicts with another request (perhaps due to using the same idempotent key). |
|            429 - Too Many Requests | Too many requests hit the API too quickly. We recommend an exponential backoff of your requests. |
| 500, 502, 503, 504 - Server Errors | Something went wrong on server's end. (These are rare.) |