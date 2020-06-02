# asyncio-example

Small example in-memory key-value store to demonstrate asyncio. It can be used as follows.

First, start the server:
```bash
python main.py
```

Second, make calls to the server in a separate terminal window (by, for example, using netcat):
```bash
nc 127.0.0.1 4040
```

You can send the following messages/operations to the server:

* `set <key> <val>`: sets key/value pair
* `get <key>`: gets value based on key
* `mset <key1> <val1> <key2> <val2>`: sets multiple key/value pairs
* `mget <key1> <key2>`: gets multiple values based on keys
* `exists <key>`: returns whether key exists or not
* `setexists <key> <val2>`: sets key/value pair in case key exists
* `setnotexists <key3> <val>`: sets key/value pair in case key does not exist
* `cset <key> <old_val> <new_val>`: sets key/value pair only if value matches 
* `inc <key>`: increments existing key by 1 (value has to be of type int)
* `dec <key>`: decrements existing key by 1 (value has to be of type int)
* `incby <key> <n>`: increments existing key by *n* (value has to be of type int)
* `decby <key> <n>`: decrements existing key by *n* (value has to be of type int)
* `list`: shows available operations

Operation names are case-insensitive.

Close the server anytime by using `CTRL + C`.
