#### Python을 이용한 간략 Web Server
Python을 이용하여 간단한 Web Server를 구성하려 한다. 내부 결과를 Web Browser를 통해 볼 수 있도록 하며, 이를 통해 Python의 Web Server 구현과 Http에 대한 이해를 높일 것이다.
###### Reference
 - [웹페이지를 통해 내 PC의 프로그램 상태 모니터하기](https://wiki.changwoo.pe.kr/project:downloadmonitor)
 - [국민내비 김기사와 Python](https://drive.google.com/file/d/0B2PzpeLe8OqBMHJmWk4zZ0MwTk0/edit?usp=sharing)

##### Web Server 구동하기
Python3에서는 다음과 같이 간단히 확인할 수 있다. 아래를 실행하고 `http://localhost:8000/`, 내 컴퓨터의 파일들을(DOS에서는 'C:\Users\heuser' ) 보여준다. 

``` shell 
python -m http.server 8000

```

