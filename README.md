# abstract-encoding

A encoding interface for node

## API

#### `buffer = encoding.encode(obj, [buffer], [offset])`

Should encode an object into a buffer. If a buffer is passed as the second argument the object should be encoded into that buffer. Otherwise a new buffer should be allocated. If an offset is passed as the third argument the object should be encoded at that byte offset. The byte offset defaults to `0`

After encoding `encoding.encode.bytes` should be set to the amount of
bytes used to encode the object.

#### `obj = encoding.decode(buffer, [offset])`

Should decode an object from a buffer. If an offset is passed as the second argument the object should be decoded from that byte offset. The byte offset defaults to `0`.

After decoding `encoding.decode.bytes` should be set to the amount of bytes used to decode the object

#### `length = encoding.encodingLength(obj)`

Should return the amount of bytes needed to encode `obj`.

## Modules that use this interface

* [protocol-buffers](https://github.com/mafintosh/protocol-buffers)
* [varint](https://github.com/chrisdickinson/varint)
* [ip-packet](https://github.com/mafintosh/ip-packet)
* [vstruct](https://github.com/dominictarr/varstruct)
* [objectstruct](https://github.com/mafintosh/objectstruct)

## License

MIT
