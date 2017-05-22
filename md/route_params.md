## Routing params
```python
from aiohttp import web


async def get_one_event(request):
    id = int(request.match_info['id'])
    event = await get_event(id)
    return web.json_response(event)


app = web.Application()
app.router.add_get(
    '/events/{id:\d+}/', get_one_event, name='one_event'
)
```
