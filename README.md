python-syncthing
================

[![pypi](https://img.shields.io/pypi/v/syncthing.svg?style=flat)](https://pypi.python.org/pypi/syncthing)
[![Syncthing](https://img.shields.io/badge/syncthing-0.14.19-blue.svg?style=flat)](https://syncthing.net)
[![Documentation Status](https://readthedocs.org/projects/python-syncthing/badge/?version=latest)](http://python-syncthing.readthedocs.io/en/latest/?badge=latest)
[![MIT License](https://img.shields.io/github/license/blakev/python-syncthing.svg?style=flat)](https://github.com/blakev/python-syncthing/blob/master/LICENSE)


Python bindings to the Syncthing REST interface.

- [Syncthing](https://syncthing.net/)
- [Syncthing REST Documentation]()
- [Syncthing Forums](https://forum.syncthing.net/)


## Running Tests

The API doctests rely on the following function to run against your instance.
None of the "breaking" calls will be tested. You must set the following environment
variables otherwise all tests will fail.

```python
def _syncthing():
    KEY = os.getenv('SYNCTHING_API_KEY')
    HOST = os.getenv('SYNCTHING_HOST', '127.0.0.1')
    PORT = os.getenv('SYNCTHING_PORT', 8384)
    IS_HTTPS = bool(int(os.getenv('SYNCTHING_HTTPS', '0')))
    SSL_CERT_FILE = os.getenv('SYNCTHING_CERT_FILE')
    return Syncthing(KEY, HOST, PORT, 10.0, IS_HTTPS, SSL_CERT_FILE)
```

## License

> The MIT License (MIT)
>
> Copyright (c) 2015-2016 Blake VandeMerwe
>
> Permission is hereby granted, free of charge, to any person obtaining a copy
> of this software and associated documentation files (the "Software"), to deal
> in the Software without restriction, including without limitation the rights
> to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
> copies of the Software, and to permit persons to whom the Software is
> furnished to do so, subject to the following conditions:
> The above copyright notice and this permission notice shall be included in all
> copies or substantial portions of the Software.
>
> THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
> IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
> FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
> AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
> LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
> OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
> SOFTWARE.
