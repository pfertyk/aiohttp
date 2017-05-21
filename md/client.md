```python
import aiohttp


async with aiohttp.ClientSession() as session:
    async with session.get('http://api.com/events/') as resp:
        print(resp.status)
        print(await resp.text())
```
