# Anubis

Continuous Integration. Continuous Delivery. Continuous Deploy.

## Architecture

- Containers as first-class
- Database:
- Frontend: NodeJS
- Routing (API): Elixir or Go
- Services: Any Language (API driven)

## API Endpoints `/api`

- Version API, in the URL `/api/v.1.0/`

### `/database`
|METHOD  | PATH  | RETURN CODE   | PARAMS  |   |
|---:|---|---|---|---|
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
|METHOD  | PATH  | RETURN CODE   | PARAMS  |   |
|---:|---|---|---|---|
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
|METHOD  | PATH  | RETURN CODE   | PARAMS  |   |
|---:|---|---|---|---|
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
|METHOD  | PATH  | RETURN CODE   | PARAMS  |   |
|---:|---|---|---|---|
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
|METHOD  | PATH  | RETURN CODE   | PARAMS  |   |
|---:|---|---|---|---|
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
|METHOD  | PATH  | RETURN CODE   | PARAMS  |   |
|---:|---|---|---|---|
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
|METHOD  | PATH  | RETURN CODE   | PARAMS  |   |
|---:|---|---|---|---|
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
    "/apples": [
      "token",
      "type"
    ]
  }
}
```
