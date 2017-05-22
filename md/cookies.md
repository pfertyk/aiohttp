## Cookies
```python
url = 'http://api.com/cookies'
cookies = {'cookies_are': 'working'}


async with ClientSession(cookies=cookies) as session:
    async with session.get(url) as resp:
        assert await resp.json() == {
           "cookies": {"cookies_are": "working"}
        }
        # ClientSession.cookie_jar
```
