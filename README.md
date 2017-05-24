# Anubis

Continuous Integration. Continuous Delivery. Continuous Deploy.

## TODO
- [ ] Plugin Specification/API
- [ ] Service Specification/API

## Architecture

- Containers as first-class
- Database: CouchDB
- Frontend: NodeJS
- Routing (API): Elixir or Go
- Services: Any Language (API driven)
- Desktop: Electron

## API Endpoints `/api`

- Version API, in the URL `/api/v.1.0/`


### `/database`
Direct interaction with the database.

|METHOD  | PATH  | RETURN CODE | PARAMS | NOTES |
|-------:|-------|-------------|--------|-------|
|GET   |  |   |   |   |
|PUT   |   |   |   |   |
|POST   |   |   |   |   |
|DELETE   |   |   |   |   |
|HEAD | | | | |
|PATCH | | | | |
|OPTIONS | | | | |
|TRACE | | | | |
|CONNECT | | | | |


### `/user`
Interact with user accounts.

|METHOD  | PATH  | RETURN CODE | PARAMS | NOTES |
|-------:|-------|-------------|--------|-------|
|GET   |  |   |   |   |
|PUT   |   |   |   |   |
|POST   |   |   |   |   |
|DELETE   |   |   |   |   |
|HEAD | | | | |
|PATCH | | | | |
|OPTIONS | | | | |
|TRACE | | | | |
|CONNECT | | | | |

### `/group`
Interact with user groups.

|METHOD  | PATH  | RETURN CODE | PARAMS | NOTES |
|-------:|-------|-------------|--------|-------|
|GET   |  |   |   |   |
|PUT   |   |   |   |   |
|POST   |   |   |   |   |
|DELETE   |   |   |   |   |
|HEAD | | | | |
|PATCH | | | | |
|OPTIONS | | | | |
|TRACE | | | | |
|CONNECT | | | | |

### `/secrets`
Access to a built-in key/value store.

|METHOD  | PATH  | RETURN CODE | PARAMS | NOTES |
|-------:|-------|-------------|--------|-------|
|GET   |  |   |   |   |
|PUT   |   |   |   |   |
|POST   |   |   |   |   |
|DELETE   |   |   |   |   |
|HEAD | | | | |
|PATCH | | | | |
|OPTIONS | | | | |
|TRACE | | | | |
|CONNECT | | | | |

### `/metrics`
Provides overall build metrics (num of jobs, num of running jobs, etc).

|METHOD  | PATH  | RETURN CODE | PARAMS | NOTES |
|-------:|-------|-------------|--------|-------|
|GET   |  |   |   |   |
|PUT   |   |   |   |   |
|POST   |   |   |   |   |
|DELETE   |   |   |   |   |
|HEAD | | | | |
|PATCH | | | | |
|OPTIONS | | | | |
|TRACE | | | | |
|CONNECT | | | | |

### `/plugin`
Used to interact with plugins.

|METHOD  | PATH  | RETURN CODE | PARAMS | NOTES |
|-------:|-------|-------------|--------|-------|
|GET   |  |   |   |   |
|PUT   |   |   |   |   |
|POST   |   |   |   |   |
|DELETE   |   |   |   |   |
|HEAD | | | | |
|PATCH | | | | |
|OPTIONS | | | | |
|TRACE | | | | |
|CONNECT | | | | |

### `/service`
Used by the API routing layer to call individual services.

|METHOD  | PATH  | RETURN CODE | PARAMS | NOTES |
|-------:|-------|-------------|--------|-------|
|GET   |  |   |   |   |
|PUT   |   |   |   |   |
|POST   |   |   |   |   |
|DELETE   |   |   |   |   |
|HEAD | | | | |
|PATCH | | | | |
|OPTIONS | | | | |
|TRACE | | | | |
|CONNECT | | | | |

### `/stream`
Interacting with the global pub/sub system.

|METHOD  | PATH  | RETURN CODE | PARAMS | NOTES |
|-------:|-------|-------------|--------|-------|
|GET   |  |   |   |   |
|PUT   |   |   |   |   |
|POST   |   |   |   |   |
|DELETE   |   |   |   |   |
|HEAD | | | | |
|PATCH | | | | |
|OPTIONS | | | | |
|TRACE | | | | |
|CONNECT | | | | |

### `/job`
Interacting with individual jobs.

|METHOD  | PATH  | RETURN CODE | PARAMS | NOTES |
|-------:|-------|-------------|--------|-------|
|GET   |  |   |   |   |
|PUT   |   |   |   |   |
|POST   |   |   |   |   |
|DELETE   |   |   |   |   |
|HEAD | | | | |
|PATCH | | | | |
|OPTIONS | | | | |
|TRACE | | | | |
|CONNECT | | | | |

### `/build`
Interacting with previously, or currently executed jobs.

|METHOD  | PATH  | RETURN CODE | PARAMS | NOTES |
|-------:|-------|-------------|--------|-------|
|GET   |  |   |   |   |
|PUT   |   |   |   |   |
|POST   |   |   |   |   |
|DELETE   |   |   |   |   |
|HEAD | | | | |
|PATCH | | | | |
|OPTIONS | | | | |
|TRACE | | | | |
|CONNECT | | | | |

### `/about`
Provides information about the current Anubis API.
This could also include the `/about` of each service, as well.

|METHOD  | PATH  | RETURN CODE | PARAMS | NOTES |
|-------:|-------|-------------|--------|-------|
|GET   |  |   |   |   |
|PUT   |   |   |   |   |
|POST   |   |   |   |   |
|DELETE   |   |   |   |   |
|HEAD | | | | |
|PATCH | | | | |
|OPTIONS | | | | |
|TRACE | | | | |
|CONNECT | | | | |


## Plugins

Example, `/api/v.1.0/plugin/[plugin_id]/help`

- All plugins will have a `/help` -- essentially a manpage
- All plugins will have a `/route`, which defines

```json
{
  "routes": {
    "/apples": {
      "params": [
        "token",
        "type"
      ]
    }
  }
}
```
