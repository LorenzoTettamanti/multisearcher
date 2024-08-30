MultiSearcher
---

MultiSearcher is an open source scan which uses some engines
to find web sites with the use of keywords and phrases

### Dependencies
* Docker to run via container with no dependencies

or 

* Python 3.x
* requests
* BeautifulSoup

Usage
----

```
$ git clone https://github.com/girorme/multisearcher.git 
$ cd multisearcher
$ pip install -r requirements.txt
```

Basic usage:
```
$ python multisearcher.py -f word_file -o output_file -t threads
```

the output file will be created in `output/` directory
	
The words in the word_file are separated by a end_line:

```
work /wp-content/
products index.php?option=
...
```

Or full help:
```
$ python multisearcher.py -h
```

Usage via docker
----
```
$ docker build -t msearch .
$ docker run --rm -v "$(pwd)":/code msearch -f words.txt -t 10
```

### License
```
The MIT License (MIT)

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
