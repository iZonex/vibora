Vibora (Work in progress)
-------------------------
![CircleCI](https://circleci.com/gh/vibora-io/vibora.svg?style=shield)

[Vibora](https://vibora.io) is a **sexy and fast** async Python 3.6+ http client/server framework.


Server Features
---------------
* Performance (https://vibora.io/#benchmarks).
* Schemas Engine. (50x faster than marshmallow, Async Enabled)
* Nested Blueprints / Domain Based Routes / Components
* Connection Reaper / Self-Healing Workers
* Sessions (files, Redis, Memcache)
* Streaming
* Websockets
* Caching tools
* Async Template Engine (hot-reloading, deep inheritance)
* Complete flow customization
* Static Files (Smart Cache, Range, LastModified, ETags)
* Complete Test Framework
* Type hints, type hints, type hints everywhere.
* Zero dependencies mode. ("pip install vibora[pure]")


Client Features
---------------
* Fastest Python HTTP client.
* Streaming MultipartForms (Inspired by: https://github.com/requests/requests/issues/1584)
* Rate Limiting / Retries mechanisms
* Websockets
* Keep-Alive & Connection Pooling
* Sessions with cookies persistence
* Basic/digest Authentication
* Transparent Content Decoding


Usage Example
-------------
```python
from vibora import Vibora
from vibora.request import Request
from vibora.responses import JsonResponse

app = Vibora()


@app.route('/')
async def home(request: Request):
    print(request.headers)
    return JsonResponse({'hello': 'world'})


if __name__ == '__main__':
    app.run(debug=True)
```


Documentation
-------------
[Check it out at Vibora Docs website](https://docs.vibora.io/docs).


Goals
-----
* **Be the fastest Python http client/server framework.**.
* Windows / Linux / MacOS.
* Enjoyable and up to date development features/trends.


Coming Soon
-----------
* Server Rate Limiting
* Cluster-Wide publish/subscribe events API.
* Auto Reloading
* JIT optimizer for user routes.
* HTTP2 Support
* Brotli Decompression
* OCSP SSL.
* Cython compiled templates.
* Async ORM
