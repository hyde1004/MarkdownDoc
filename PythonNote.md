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