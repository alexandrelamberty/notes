# Redis

## Security

## Redis CLI

### Connection

### Commands

List all the keys
```bash
keys *
```

Get the type of a key 
```bash
type <key>
```
and depending on the response perform:

String
```bash
get <key>
```

Hash
```bash
hgetall <key>
```

List
```bash
lrange <key> 0 -1
```

Set
```bash
smembers <key>
```

Zset
```bash
zrange <key> 0 -1 withscores
```
to get the content of a key

### Tools

- [Redis Commander](https://github.com/joeferner/redis-commander)
