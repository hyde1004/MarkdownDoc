#### Python Module

##### urllib
###### python3에서 urllib2는 urllib에 흡수되었다.

urllib는 다음 모듈을 모아 놓은 패키지이다.

- urllib.request for opening and reading URLs
- urllib.error containing the exceptions raised by urllib.request
- urllib.parse for parsing URLs
- urllib.robotparser for parsing robots.txt files

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
`urlopen()`은 url 또는 `Request`객체를 인자로 받는다. `Request` 객체를 사용하면, POST mehtod를 사용하거나, header를 추가할 수 있다. `urlopen()`에 data를 넘기면 POST method로 수행된다.

``` python
import urllib.request
url = 'http://dna.daum.net'
data = urllib.parse.urlencode({'spam':1, 'eggs':2})
data = data.encode('utf-8')
req1 = urllib.request.Request(url)
response = urllib.request.urlopen(url, data)
```
##### urllib.request
###### 출처 : https://docs.python.org/3/library/urllib.request.html#module-urllib.request

urllib.request는 URL관련한 열기, 인증, 쿠키 등에 대한 클래스와 함수를 정의한다.

#### urllib.parse
###### Reference
 - 
``` python
# Class
urllib.request.Request(url, data=None, headers={}, origin_req_host=None, unverifiable=False, method=None)

# Function
urllib.request.urlopen(url, data=None, [timeout, ]*, cafile=None, capath=None, cadefault=False)
```
기본 사용형태는 다음과 같다
``` python
import urllib.request

url = "http://www.naver.com"

req = urllib.request.Request(url)
response = urllib.request.urlopen(req)

result = response.read().decode('utf-8')
```

#### BeautifulSoup4
###### Reference
 - [BeautifulSoup4 번역문서](http://coreapython.hosting.paran.com/etc/beautifulsoup4.html)
 - [How to find tags with only certain attributes - BeautifulSoup](http://stackoverflow.com/questions/8933863/how-to-find-tags-with-only-certain-attributes-beautifulsoup)

기본 사용방법은 html문서를 BeautfilSoup에 넣어주면 된다.

``` python
import bs4

soup = bs4.BeautifulSoup(html_doc)

print(soup.prettify())  # 보기 좋게 출력

soup.title		# title tag에 접근
soup.body		# body tag에 접근

for talk in soup.find_all('div', {'class':'talk'}):  # div tag의 속성으로 검색
	print(talk.span.text)
# <div class=\'talk\'><span>Mom: How was school today, Sam?</span></div>

```