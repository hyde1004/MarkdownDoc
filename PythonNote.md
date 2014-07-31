#### Python Note

##### 정수 나눗셈
``` python
3 / 2 # 1.5
3 // 2 # 1
```

##### List Comprehension
아래에서 결국엔 `len(n)`으로 List가 채워진다.
``` python
len_cycles = [len(n) for n in cycles]
```

##### Directory operators
https://docs.python.org/3.4/library/pathlib.html#basic-use

##### zip function
여러 리스트를 김밥말듯 말아서, 자른다.
```python
a = [1, 2, 3, 4, 5]
b = ['a', 'e', 'i', 'o', 'u']
for x, y in zip(a, b):
	print(x, y)

1 a
2 e
3 i
4 o
5 u    
```

##### import 사용법
``` python
# import 파일명 형태
import module1
module1.hello()

# from 파일명 import 함수명 형태 (파일명 생략가능)
from module1 import hello() 
```

`if __name__ == '__main__'` 구문은 파일 단독으로 실행하는 경우만 동작하고, 다른 파일에서 재사용할때는 동작하지 않는 부분이다.