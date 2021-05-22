# randomstuff.py
An easy to use python API wrapper for the Random Stuff API.

## Quickstart
Firstly make sure to [get the API key from here](https://api.pgamerx.com/register)

Here are few examples to get you started.

### Getting AI response
```py
import randomstuff

client = randomstuff.Client(key='api-key-here')

response = client.get_ai_response("Hi there")
client.close()
print(response)
```

### Getting random joke
```py
import randomstuff

client = randomstuff.Client(key='api-key-here')

response = client.get_joke(type="any")
client.close()
print(response.joke)
```

### Getting random image
```py
import randomstuff

client = randomstuff.Client(key='api-key-here')

response = client.get_joke(type="any")
client.close()
print(response)
```

## Async Support
This library also supports async usage.
```py
import randomstuff

client = randomstuff.AsyncClient()

def coro():
  response = await client.get_ai_response("Hello world")
  await client.close()  
  print(response)
```
