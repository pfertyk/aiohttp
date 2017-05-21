```python
from aiohttp import web


async def get_all_events(request):
    events = await get_events()
    return web.json_response(events)


def app_factory(args=()):
    app = web.Application()
    app.router.add_get(
        '/events/', get_all_events, name='all_events'
    )
    return app
```
