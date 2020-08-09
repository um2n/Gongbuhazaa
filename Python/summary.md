# ___Python___  



## 1. 사칙연산  
> 출력은 ```pirnt()``` 사용  
>   >   두 개 출력 시 ```,```로 구분  


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




