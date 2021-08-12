# ___Python___  



## 1. 사칙연산  
> 출력은 ```pirnt()``` 사용  
>   >   두 개 출력 시 ```,```로 구분  

> 출력 끝 지정 
print('', end='')  
>   > ' ', '-', '\n'(줄바꿈), '\t'(탭)  
>   >   > \n을 출력하고 싶을 땐 \\\n을 입력.
'을 출력하고 싶을 땐 '앞에 \입력  




    덧  셈 - print(1 + 2) 
    뺄  셈 - print(1 - 2)  
    곱  셈 - print(1 * 2)  
    나눗셈 - print(1 / 2)  
    제  곱 - print(1 ** 2)  
      몫 - print(1 // 2)  
    나머지 - print(1 % 2)  

   

  
<br/>

## 2. 변수  
> '='을 기준으로 오른쪽 값이 왼쪽 변수에 저장됨 


<b>변수 이름</b>

    1. 숫자로 시작 x  
    2. 빈칸 사용 x  


<br/>  

## 3. 할당 연산자  
    a+=b : a=a+b
    a-=b : a=a-b  
    a*=b : a=a*b  
    a/=b : a=a/b  

>   ex) ```i+=1``` : i+1  


<br/>

## 4. 문자열(String)  
> ```''```이나 ```""``` 안에 숫자나 문자를 넣으면 문자열이 됨

<b> 문자열 연산 </b>  

```  
my_str1 = 'a' + 'b' + 'c' 

=> abc  

my_str2 = 'abc' * 4  (숫자만 가능 - 반복)  

=> abcabcabcabc
```  

<b> 인덱싱 </b>  

> 양수는 앞에서부터 0  

```  
alphabet = 'abcde'  
print(alphabet[0])  

=> a  
```

> 음수는 뒤에서부터 -1  

```
alphabet = 'abcde'  
print(alphabet[-1])

=> e 
``` 

<b> 슬라이싱 </b>  

> a:b = a에서 b 전까지

``` 
alphabet = 'abc de'  
print(alphabet[0:1])  

=> a 

print(alphabet[0:2])  

=> ab  
```

> 공백 포함 
```
print(alphabet[3:6])  

=> c de  
```  

<b> 숫자 생략하기 </b>  

> [:a] = a 전까지  
[b:] = b부터  

```
alphabet = 'abcde'
print(alphabet[:3])  

=> abc  

print(alphabet[2:])

=> cde  
```

<b> 포맷팅 </b>  

```
print('Life is {}'.format('Short!'))  

=> Life is Short!  

print('{} X {} = {}'.format(2,3,2*3))  

=> 2 X 3 = 6  
```

> c스타일 포맷팅  
%d, %f, %s  \
```
print('Life is %s' % 'Short!')  

print('%d X %d = %d' & (2, 3, 2 * 3)) 
```

<b> 여러줄 문자열 </b>  

>  ``` ``` 나 """ 을 사용하면 여러 줄을 입력할 수 있게 됨. (enter키 사용 가능) 

</br>  

## 5. 주석  

: #을 사용한다.  


</br>  

## 6. 리스트  
: 여러개의 값들을 한번에 저장  
```
my_list1 = []  
my_list2 = [1, 2, 3]  
my_list3 = ['a', 'b']  
```  

<b>리스트에 값 추가하기 </b>  

> ```append``` 사용  

```
my_list = []  
my_list.append =(123)
my_list.append('abc')  
my_list.append(True)  

=> [123, 'abc', True]  
```  

<b> 인덱싱 </b>  

> 값을 바꿀 수 있다.  


```  
my_list[0] = 3.14  
my_list[1] = 'ABC'  
my_list[-1]= False  

=> [3.14, 'ABC', False]  
```  


<b> del </b>  

> 값을 제거할 수 있다.  
> 변수 이름으로 사용할 수 없다.  

``` 
del my_list[0]    

=> ['abc', True]  
```  
_0이 삭제되면 그 뒤에 있는 값이 0이 됨_  


<b> 슬라이싱 </b>  

> 앞 숫자 : 그 숫자부터 시작, 뒷 숫자 : 그 숫자의 전까지 가져옴  

```
my_list = ['a', 'b', 'c']  

print(my_list[:1])  
print(my_ist[1:3]) 
print(my_list[2:])  

=> ['a'], ['b', 'c'], ['c'] 
``` 


<b> .sort() </b>  

> 정렬  

```
my_list = [3, 2, 4, 1]  
my_list.sort()
print(my_list)  

=> [1, 2, 3, 4]  
```  


<b> .count() </b>  

> 요소의 개수를 센다.  

```
my_list = 'a', 'c', 'a', 'b']  
print(my_list.count('a'))  
print(my_list.count('b'))  
print(my_list.count('c'))  

=> 2, 1, 1  
```  


<b> in </b>  

> 리스트 안에 어떤 값의 유무를 확인한다.  

```
my_list = 'a', 'b', 'c', 'd']  
print('a' in my_list)  
print('f' not in my_list)  

=> True, True
```  

</br>  

## 7. 튜플  

: 값을 변경할 수 없다.  
> ()을 사용하거나 ,만 사용한다.  

```
my_tuple1 = ()  
my_tuple2 = (1,)  
my_tuple3 = ('a', 'b', 'c')  
my_tuple4 = 3.14, 'Python', True  

=> (), (1), ('a','b','c'), (3.14,'Python', True)
```
_값이 하나일 때는 튜플이라는 것을 알려주기 위해 ,과 )를 사용한다_  


</br>

<b> 튜플을 사용하는 이유 </b>

: 값을 변경할 수 없어서 신뢰성이 높다.  
리스트보다 빠르다.  


</br>  

## 8. 패킹 / 언패킹  

: 여러 개의 값을 하나로 묶거나 푸는 것  

```
my_tuple = 3.14, 'Python', Flase 
-> 패킹  

i, s, b = (123, 'abc', True)  
-> 언패킹   
```   

</br>  

## 9. 반복   
</br>

<b> ```for```</b>

 : 횟수로 반복하기 


```for``` 변수 ```in``` 순서열 ```:```    명령1    명령2 ```  
_:와 명령 사이, 명령과 명령 사이에 띄어쓰기 4칸(Tab)_  

1.
```
my_list = [1, 2, 3]  
for count in my_list :    print('횟수:', count)  

=> 횟수 : 1  
횟수 : 2  
횟수: 3  
```  
2.

```
my_str = 'coding'  
for letter in my_str :    print('문자:', letter)  

=> 문자 : c
문자 : o  
문자 : d  
문자 : i  
문자 : n  
문자 : g  
```  

<b> ```range(stop)``` </b> 

: stop전까지의 순서열을 만들어준다. 

```
for count in range(3) :    print('횟수:', count)  

=> 횟수 : 0  
횟수 : 1  
횟수 : 2  
```

<b> ```range(strat, stop)``` </b>

: start부터 stop전까지의 순서열을 만들어준다.


```
for count in range(5,10):    '횟수:', count

=> 횟수 : 5
횟수 : 6
횟수 : 7
횟수 : 8
횟수 : 9
```

<b> for 중첩하기 </b>  

```
for j in range(2) :
for i in range(2) :
print('i:{}, j:{}'.format(i,j))

=> i:0, j:0
i:1, j:0
i:0, j:1
i:1, j:1
```


</br>  

## 10. 













