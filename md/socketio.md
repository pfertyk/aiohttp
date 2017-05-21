```python
from aiohttp import web
import socketio

sio = socketio.AsyncServer()
app = web.Application()
sio.attach(app)

@sio.on('message')
async def message(sid, data):
    print('message', data, 'room', sid)
    await sio.emit('reply', data)


web.run_app(app, host='127.0.0.1', port=8080)
```
