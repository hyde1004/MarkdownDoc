#### Python Module

##### urllib
###### python3에서 urllib2는 urllib에 흡수되었다.

urllib는 url처리 모듈이다.
다음은 가장 간단한 사용방법이다.

``` python
# code from https://docs.python.org/3/howto/urllib2.html
import urllib.request
url = 'http://dna.daum.net'

response = urllib.request.urlopen(url) # file open과 유사
html = response.read()
response.close()
```