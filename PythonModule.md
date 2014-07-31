#### Python Module

##### urllib
###### python3에서 urllib2는 urllib에 흡수되었다.

urllib는 url처리 모듈이다.
다음은 가장 간단한 사용방법이다.

``` python
# code from http://dna.daum.net/tools/python/tutorial
import urllib
url = 'http://dna.daum.net'

u = urllib.request.urlopen(url)
data = u.read() # u is a file-like object
```