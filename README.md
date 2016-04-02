# abstract-encoding

A encoding interface for node

## Badge

[![abstract-encoding](https://img.shields.io/badge/abstract--encoding-compliant-brightgreen.svg?style=flat)](https://github.com/mafintosh/abstract-encoding)

```
[![abstract-encoding](https://img.shields.io/badge/abstract--encoding-compliant-brightgreen.svg?style=flat)](https://github.com/mafintosh/abstract-encoding)
```

## API

#### `buffer = encoding.encode(obj, [buffer], [offset])`

Should encode an object into a buffer. If a buffer is passed as the second argument the object should be encoded into that buffer. Otherwise a new buffer should be allocated. If an offset is passed as the third argument the object should be encoded at that byte offset. The byte offset defaults to `0`

After encoding `encoding.encode.bytes` should be set to the amount of
bytes used to encode the object.

#### `obj = encoding.decode(buffer, [start], [end])`

Should decode an object from a buffer. If a start-offset is passed as the second argument the object should be decoded from that byte offset. The start-offset defaults to `0`. An end-offset can be passed as the third argument specifying at which byte to end the decoding (not including the byte at the end-offset). The end defaults to `buffer.length`.

After decoding `encoding.decode.bytes` should be set to the amount of bytes used to decode the object

#### `length = encoding.encodingLength(obj)`

Should return the amount of bytes needed to encode `obj`.

## Modules that use this interface

* [protocol-buffers](https://github.com/mafintosh/protocol-buffers)
* [varint](https://github.com/chrisdickinson/varint)
* [varuint-bitcoin](https://github.com/fanatid/varuint-bitcoin)
* [ip-packet](https://github.com/mafintosh/ip-packet)
* [varstruct](https://github.com/dominictarr/varstruct)
* [varstruct-match](https://github.com/dominictarr/varstruct-match)
* [objectstruct](https://github.com/mafintosh/objectstruct)
* [mdns-txt](https://github.com/watson/mdns-txt)
* [base64-emoji](https://github.com/watson/base64-emoji)
* [uint64be](https://github.com/mafintosh/uint64be)
* [uint48be](https://github.com/mafintosh/uint48be)
* [mp4-box-encoding](https://github.com/jhiesey/mp4-box-encoding)
* [bencode](https://github.com/themasch/node-bencode)
* [bencode.js](https://github.com/fanatid/bencode.js)
* [bitfield-rle](https://github.com/mafintosh/bitfield-rle)

## License

MIT
