# What is this?

This is effectively a fork of [this repo](https://github.com/chiefbiiko/sha256) but with the imports pinned down.

# Usage

``` ts
import { sha256 } from "https://deno.land/x/ez_sha256@1.0.1/main.ts"

const string = "howdy"
console.log(`SHA2-256 of ${string}`, sha256(string, "utf8", "hex"))
```

## API

#### `new SHA256()`

Creates a new SHA2-256 instance.

#### `SHA256#init(): SHA256`

Initializes a hash instance.

#### `SHA256#update(msg: string | Uint8Array, inputEncoding?: string): SHA256`

Updates a hash with additional data. `inputEncoding` can be one of `"utf8"`, `"hex"`, or `"base64"`.

#### `SHA256#digest(outputEncoding?: string): string | Uint8Array`

Finalizes the hash. `outputEncoding` can be one of `"utf8"`, `"hex"`, or `"base64"`. If it is omitted a `Uint8Array` is returned.

#### `sha256(msg: string | Uint8Array, inputEncoding?: string, outputEncoding?: string): Uint8Array`

Convenience function for hashing singular data.

## License

[MIT](./LICENSE)
