```python
import asyncio
from aiohttp import web

async def handler(request):
    return web.Response(text="OK")

async def main(loop):
    server = web.Server(handler)
    await loop.create_server(server, "127.0.0.1", 8080)
    await asyncio.sleep(100*3600)

loop = asyncio.get_event_loop()
loop.run_until_complete(main(loop))
loop.close()
```
