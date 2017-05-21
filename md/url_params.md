```python
p = {'key': 'value'}

async with session.get('http://api.com/', params=p) as resp:
    assert resp.url == 'http://api.com/?key=value'
```
