#### Python 3와 한글
###### Reference


``` python
a = '—' # EM DASH     # <class 'str'>
b = a.encode('utf-8') # b'\xe2\x80\x94'  <class 'bytes'>
c = b.decode('utf-8') # '—' <class 'str'>
print(b)              # b'\xe2\x80\x94'
print(c)              # UnicodeEncodeError: 'cp949' codec can't encode character '\u2014' in position 0: illegal multibyte sequence
```
