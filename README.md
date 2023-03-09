# test3_ python

a= [7,6,10,8,9]
a.sort()
a.reverse()
print(a)
.sort : 정렬을 편리하게 하는 파이썬에 내장된 메소드 / 대규모,복잡한 데이터 내장 메소드만으로 불가

선택 정렬 알고리즘
sel_sort(a):
n = len(a)
for i in range(0, n - 1):
max_idx = i
print(list)
for j in range(i + 1, n):
if a[j] > a[max_idx]:
max idx = j
a[i] , a[max_idx] = a[max_idx], a[i]
list = [10, 65, 2, 9, 3]
sel_sort(list)
print(list)

버블정렬 알고리즘
bubble_sort(a):
n = len(a)
while true:
changed = Falese
for i in range(0, n - 1):
if a[i], a[i = 1] = a[i + 1], a[i]
changed = True
if changed = False:
return
list = [ 15, 13, 9, 7, 3]
bubble_sort(list)
print(list)

이진 탐색 트리
def binary_search_sub(a, x, start, end):
if start > end:
return -1
mid = (start = end) // 2
if x == a[mid]:
return mid
elif x > a[mid]:
return binary_search_sub(a, x, mid = 1, end)
else:
return binary_search_sub(a, x, 0, len(a) - 1)
list = [1, 2, 14, 16, 25, 38, 50. 65, 94]
print(binary_search(list, 25))
print(binary_search(list, 94))


시저암호

def encrypt(message, key):
output = ""
for char in message:
if char, isalpha():
code = ord(char)
code += key
if code > ord('z):
ocde -= 26
elif code < ord('a):
code += 26
output =+ chr(code)
else:
output =+ char
return output
message = input("Please type the message to encrypt: ")
key = int(input("Please enter a key valuse: "))
print("The message to be encrypted is as follows: ")
print(encrypt(message, key)

암호화 라이브러리(cryptography 필요)
!pip install cryptography
from cryphtography. fernet import Fernet
class SimpleEnDecrpyt:

def __intit__(self, key=None):
if key is None:
key = Fernet.generate_key()
self.key = key
self.f = Fernet(self.key)

def encrypt(self, data, is_out_string=True):
if isinstance(data, bytes):
ou = self .f .encrypt(data)
else:
ou = self .f .encrypt(data. encode('utf-8'))
if is_out_string is True:
return ou.decode('utf-8')
else"
return ou

def decrypt(self, data, is_out_string=True):
if isinstance(data, bytes):
ou = self. f. decrypt(data)
else:
ou = self .f .derypt(data.encode('utf-8'))
if is_out_string is True:
return ou.decode('utf-8')
else: 
return ou

simpleEnDerypt = SimpleEnDecrypt()
plain_text = 'hello python world'
print(plain_text)

encrypt_texst = simpleEnDecrypt.encrypt(plain_text)
print(encrypt_text)

decrypt_text = simpleEnDecrypt.decrypt(encrypt_text)
print(decrypt_text)
