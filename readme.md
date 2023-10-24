# API Documentation

## Endpoints

### GET /api

Returns a list of available endpoints.

#### Response

- `200 OK` - Returns a JSON object containing a list of available endpoints.

### GET /api/retrieve

Returns a list of symbols.

#### Query Parameters

- `api_key` (required) - The API key to use for authentication.

#### Response

- `200 OK` - Returns a JSON object containing a list of symbols.

### POST /api/symbol/create

Creates a new symbol.

#### Query Parameters

- `api_key` (required) - The API key to use for authentication.

#### Request Body

- `symbol` (required) - The symbol to create.
- `name` (required) - The name of the symbol.
- `sector` (required) - The sector the symbol belongs to.
- `industry` (required) - The industry the symbol belongs to.
- `outstanding_shares` (required) - The number of outstanding shares for the symbol.

#### Response

- `200 OK` - Returns a JSON object containing status, and error message (if any).

## Authentication

All endpoints require authentication using an API key. The API key must be passed as a query parameter in the request URL.

If the API key is not valid or is missing, the endpoint will return a `401 Unauthorized` or `403 Forbidden` error.

## Permissions


If the API key does not have the required permissions, the endpoint will return a `403 Forbidden` error.

## API Documentation

API documentation is available at `/api/docs`. The documentation is provided in YAML format.
