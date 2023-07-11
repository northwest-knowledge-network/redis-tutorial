# Important commands for intereacting with redis

## redis-cli

redis-cli is a command line interface for interacting with redis. Unserstanding redis-cli is useful for understanding the redis implementation in Python.

To start, connect to your redis instance:

`redis-cli -h 127.0.0.1 -p 5020`

To see if there are any keys in the database:

`KEYS *`

To check the type of a key:

`TYPE <key>`

### ReJSON-RL (JSON) data type

As the name suggests, ReJSON stores JSON structures! Given a key of type ReJSON-RL,

`JSON.GET <key>`

returns the JSON structure.

### zset (sorted set) data type

How to query a sorted set in redis?

`ZRANGE locations 0 -1 WITHSCORES`
