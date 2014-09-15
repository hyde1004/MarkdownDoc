#### matplotlib 이용하기
###### Reference
 - [파이썬 그래프 그리기](https://wikidocs.net/1019)

그래프를 위한 모듈이다.
OS X에서 다음과 같이 설치하였다. 설치에 별다른 어려움은 없었다.
``` shell
pip3 install matploblib
```

Reference의 코드대로 입력하였더니, 잘 그려졌다.
``` python
import matplotlib.pyplot as plt 
plt.plot([1, 2, 3, 4])
plt.show()
```
