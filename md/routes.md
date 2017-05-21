```python
from aiohttp import web

def app_factory(args=()):
    app = web.Application()

    app.router.add_get(
        '/events/', get_all_events, name='all_events'
    )

    return app
```
