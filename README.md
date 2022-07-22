# ref and out keyword
`ref` tells the compiler that the object is initialized before entering the function, while `out` tells the compiler that the object will be initialized inside the function.

So while `ref` is two-ways, `out` is out-only.

# stream
Many data-structures (`lists`, `collections`, etc) act as containers - they hold a set of objects. But not a stream; if a list is a bucket, then a stream is a hose. You can pull data from a stream, or push data into a stream - but normally only once and only in one direction (there are exceptions of course). For example, TCP data over a network is a stream; you can send (or receive) chunks of data, but only in connection with the other computer, and usually only once - you can't rewind the Internet.

Streams can also manipulate data passing through them; compression streams, encryption streams, etc. But again - the underlying metaphor here is a hose of data. A file is also generally accessed (at some level) as a stream; you can access blocks of sequential data. Of course, most file systems also provide random access, so streams do offer things like Seek, Position, Length etc - but not all implementations support such. It has no meaning to seek some streams, or get the length of an open socket.
