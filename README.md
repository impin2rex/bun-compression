# bun-compression

Compression plugin for [Hono](https://github.com/honojs/hono)

## Installation

```bash
bun add bun-compressor
```

## Example

```typescript
import { Hono } from 'hono'
import { compress } from 'bun-compressor'

const app = new Hono()

app.use('*', compress())
```

## Config

### type

@default `gzip`

The type of compression to use. Can be one of the following:

- `gzip`
- `deflate`

### options

@default `{}`

Options passed to the compression library.

Refer to the bun zlib options [documentation](https://bun.sh/docs/api/utils#bun-gzipsync) for more details.

### encoding

@default `utf-8`

The encoding of the response body that is being compressed.

## Acknowledgments

The project is a fork of the original repository "bun-compression" available at [bun-compression](https://github.com/sunneydev/bun-compression). The fork aims to build upon the existing codebase, possibly adding new features, fixing bugs, or adapting the code to suit specific requirements.
