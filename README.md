<h1><img src="https://raw.githubusercontent.com/mrsmn/ares/master/doc/ares.png" height=85 alt="ares3" title="ares3">ares3</h1>

[![PyPi Version](http://img.shields.io/pypi/v/ares.svg)](https://pypi.python.org/pypi/ares/)   [![Downloads](http://img.shields.io/pypi/dm/ares.svg)](https://pypi.python.org/pypi/ares/)

**ares** is an APACHE licensed library written in Python providing an easy to use wrapper around https://cve.circl.lu.

## Installation:

From source use

        $ python setup.py install

or install from PyPi

	not supported at the moment

you will need python3 for this fork of ares.

## Documentation:

- **`GET /api/browse/`**
- **`GET /api/browse/vendor`**

```python
>>> from ares import CVESearch
>>> cve = CVESearch()
>>> cve.browse(<vendor>)
```

- **`GET /api/search/vendor/product`**

```python
>>> cve.search('microsoft/office')
```

- **`GET /api/cveid/cveid`**

```python
>>> cve.id('CVE-2014-0160')
```

- **`GET /api/last`**

```python
>>> cve.last()
```

- **`GET /api/dbInfo`**

```python
>>> cve.dbinfo()
```

- **`GET /api/cpe2.2/cpe`**

```python
>>> cve.cpe22('cpe:2.3:a:microsoft:office:2011:-:mac')
```

- **`GET /api/cpe2.3/cpe`**

```python
>>> cve.cpe23('cpe:/a:microsoft:office:2011::mac')
```

- **`GET /api/cvefor/cpe`**

```python
>>> cve.cvefor('cpe:/a:microsoft:office:2011::mac')
```

## License:

```
    Apache v2.0 License
    Copyright 2015-2016 Martin Simon

     Licensed under the Apache License, Version 2.0 (the "License");
     you may not use this file except in compliance with the License.
     You may obtain a copy of the License at

         http://www.apache.org/licenses/LICENSE-2.0

     Unless required by applicable law or agreed to in writing, software
     distributed under the License is distributed on an "AS IS" BASIS,
     WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
     See the License for the specific language governing permissions and
     limitations under the License.

```
