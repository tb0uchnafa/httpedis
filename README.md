## Htt[P|R]edis

A HTTP wrapper for `ioredis`

### Usage 

```js
const config = {
    // Redis properties 
    REDIS_HOST: "localhost",
    REDIS_PORT: 6379,
    REDIS_AUTH: "mypassword", 
    REDIS_DB: 0, 
    // Server port
    HTTP_PORT: 9001
};

const httpedis = require('httpedis')(config);

// Starts the server
httpedis.start();
```
# Enjoy
```shell 
# GET all keys 
curl -X PUT -d foo=bar "localhost:9001/set/foo" 
curl "localhost:9001/get/foo" 
curl "localhost:9001/keys/*" 
["foo"]
```
