## Custom headers
```python
import json


url = 'http://api.com/events/'
payload = {'some': 'data'}
headers = {'content-type': 'application/json'}

await session.post(
    url, data=json.dumps(payload), headers=headers
)
```
