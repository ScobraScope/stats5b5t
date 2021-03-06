
# 5b5t statistics
API wrapper for 5b5t's statistics

```pip install stats5b5t```

> **Tested on: [Python 3.9](https://www.python.org/downloads/release/python-390)**

## [Documentation](https://github.com/ScobraScope/stats5b5t-documentaition)
You can find a detailed documentation [here](https://github.com/ScobraScope/stats5b5t-documentaition)

## Usage
```py
from stats5b5t import api

stats = api.Statistics()

r = stats.request("uuid here")

print(stats.kills(r))
```

**With debugging:**

```py
from stat5b5t import api, tools

stats = api.Statistics()
tests = tools.Debugging()

r = stats.request("uuid here")

print(stats.kills(r))
print(tests.isvalid(r))
print(tests.missmatch(r))
print(tests.errmsg(r))
```

**Username instead of UUID**

```py
from stats5b5t import api

stats = api.Statistics()

uuid = stats.getuuid("playername")
r = stats.request(uuid)

print(stats.deaths(r))
```

## Modules: api, tools

> **api**

Handles requests and data sorting for you.

> **tools**

Handles debugging and checks for you.

## Updates
I will update this from time to time to add new features, and I will for sure update it whenever there are API changes to stay up to date.


