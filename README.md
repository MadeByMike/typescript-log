# TypeScript abstract logger

[![Build Status](https://travis-ci.com/sevenwestmedia-labs/typescript-log.svg?branch=master)](https://travis-ci.com/sevenwestmedia-labs/typescript-log)

Useful for libraries which want to enable the consuming application to provide a logger. Our projects ended up duplicating the same logging interface and consoleLogger and noopLogger's.

Compatible with universal applications (works in browser and node)

## Usage

```ts
import pino from 'pino'
import { consoleLogger, noopLogger, Logger } from 'typescript-log'

const pinoLogger: Logger = pino({})

const logsNothingLogger: Logger = noopLogger()
const logsToConsoleLogger: Logger = consoleLogger(
    /* optional, warn default */ 'error'
)
```

## References

Similar to https://github.com/kallaspriit/ts-log but uses `log(obj, msg)` format for the interface
