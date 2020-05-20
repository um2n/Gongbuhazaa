## JAVA  
  
_전 세계에서 가장 많이 사용하는 언어_  

***  

  
* 특징  
  
  1. ```쉬운 난이도``` (...?)  
  2. ```Garbage Collector``` : 자동으로 메모리를 정리해준다.  
  3. ```JVM(Java Virtual Machine)``` : 운영체제와 상관없이 프로그램을 실행할 수 있다.


* ```JVM(Java Virtual Machine)```  
    JAVA는 JVM이라는 프로그램을 통해 동작한다.  
    '*.java'라는 확장자로 이루어져 있는데, 이는 JAVAC Compiler를 통해 *.class파일로 변환되고, 각 운영체제의 JVM이 이 파일을 실행하는 방식으로 동작한다.  

 1. 컴퓨터에 JVM이 설치돼있지 않으면 Java 프로그램을 실행시킬 수 없다. JDK를 설치하면 JRE는 자동으로 같이 설치된다.  
 2. 같은 Java의 소스코드는 여러 운영쳋제에서 수정하지 않고 사용할 수 있다.  
    > Native Language : 특정 운영체제에서만 사용가능한 프로그래밍 언어 _C언어_  
    > Managed Language : 여러 운영체제에서 사용할 수 있는 프로그래밍 언어 _Java_  
 3. Managed Language는 Native Language보다 실행속도가 느리다.  


* ```SDT(Strict Data Type)```  
    자료형(Data Type) : 프로그래머가 Compiler에게 알려주는 데이터의 속성  

* ```POP```(C,VB, PASCAL 등)  
    프로그램이 시작하면 프로그래밍이 된 순서대로 진행하며, 모든 순서가 종료되면 프로그램 또한 종료된다.  

 1. 기능을 우선시하여 프로그래밍하므로 OOP에 비해 빠르게 프로그래밍이 가능하다.  
 2. 대부분의 함수가 전역 데이터를 사용하기 때문에 데이터 접근이 용이하다. 즉, 보안성이 낮다.  
    >_전역 데이터 : 프로그램 내부 어디에서든 사용 가능함_  
 3. 데이터의 모듈화가 어렵다.  
    >_모듈화 : 프로그램을 관리가 용이하도록 기능 단위로 분리하는 작업_  

* ```OOP```(JAVA, C++, C#, .NET 등)  
    POP의 단점을 보완하여 개발된 개념으로 ```객체```라는 개념을 통해 데이터 및 함수를 모듈화하여 프로그램의 유지 보수와 보안성을 강화했다.  

 1. ```캡슐화``` : 데이터를 캡슐화(은닉)함으로써, 프로그램 외부에서 접근 가능한 데이터를 지정할 수 있다. public, private, protected 등의 접근자를 통해 외부에서 접근 가능한 데이터의 종류를 제한할 수 있다. 따라서 데이터의 보안성이 좋아진다.  
 2. ```추상화``` : 객체의 기본적인 틀, 뼈대만 미리 만들어놓을 수 있는 기능이다.  
 3. ```상속``` : 피상속 객체(부모 클래스)의 데이터 및 함수들을 상속 객체로 그대로 이어 받아 사용할 수 있는 기능이다. 이를 통해 코드의 재사용성을 높일 수 있다.  
 4. ```다형성``` : 객체가 다양한 형태로 표현될 수 있다는 개념으로, 틀을 가진 객체가 구체화된 객체로 표현이 가능하다는 뜻이다.  



***  


### 메모리  
   1. Register : CPU 내부에서 사용되는 저장공간이다.  
   2. Storage : 가장 흔하게 사용되고 있는 것은 HDD, SSD  
   3. Memory : RAM이라고 불리는 하드웨어가 메모리 공간을 담당하며, Storage보다는 빠르지만 Register보다는 느리다. 다른 속도 및 용량을 갖고 있는 저장장소들을 보완하는 역할을 한다.  



### 연산자  
   1. 대입연산자  




   2. 산술연산자(+, -, *, /, %)



   3. 복합대입연산자(+=, -=, *=, /=, %=) : 왼쪽 값에 오른쪽 값을 산술연산한 뒤 결과 값을 왼쪽에 대입한다.  



   4. 비교연산자 : 연산자의 좌우값을 비교하는 연산자다. boolean형(T/F)으로 반환된다.  
      >== : 양측이 같다, = : 우측 값을 좌측에 대입한다. 



   5. 전위/후위 연산자(++,--) : ++는 변수의 값을 1 증가시키고, --는 변수의 값을 1 감소시킨다. 둘 다 출력 명령보다 먼저 실행된다.  



   6. 논리연산자(&&, ||, !)  
      1. ```AND(%%)``` : 좌우 값이 모두 T일 때만 T이고 그 외의 경우는 전부 F를 반환한다.  
      2. ```OR(||)``` : 좌우 값 중 하나라도 T일 경우 T를 반환한다.  
      3. ```NOT(!)``` : T를 F로, F를 T로 바꾼다.  



   7. 비트연산자 : 비트 단위의 연산을 위한 연산자다.  
      1. ```&``` : AND 연산자와 동일하다.  
      ![36097ef0632deb70bf62b90d55834d55e78ba22dc27e763753784ef89f3faafd](https://user-images.githubusercontent.com/58182440/81330457-1010de80-90db-11ea-8aad-ab9fa7ef7bd1.png)
      2. ```|``` : OR 연산자와 동일하다.  
      ![d](https://user-images.githubusercontent.com/58182440/81330520-2880f900-90db-11ea-94ae-241aea8b3b81.png)  
      3. ```^``` : 비트 간에 하나만 1일 경우 1이 된다. XOR 연산과 동일하다.  
      ![a](https://user-images.githubusercontent.com/58182440/81330620-4baba880-90db-11ea-8f0d-b109ba4a0ef2.png)
      4. ```~``` : 비트의 0과 1을 바꿔준다.  



   8. 시프트연산자  
      1. ```<<``` : 비트를 왼쪽으로 밀어낸 뒤 공백을 0으로 채운다.  
      2. ```>>``` : 비트를 오른쪽으로 밀어내지만, 밀어내기 전 가장 왼쪽 비트와 같은 숫자로 공백을 채운다.  
      3. ```>>>``` : 비트를 오른쪽으로 밀어내면서 공백을 0으로 채운다.  

   

   9. 연산자 우선순위  
   |순서|연산자|예시|   
   |:---:|:---:|:---:|   
   | 1 | 괄호 | ```(),[]``` |  
   | 2 | 전위연산자 | ```++a,--b``` |  
   | 3 | 산술연산자 | ```+,=,*,/,%``` |  
   | 4 | 시프트연산자 | ```<<,>>``` |  
   | 5 | 비교연산자 | ```<,<=,>,>=,==,!=``` |  
   | 6 | 대입연산자 | ```=,+=,-=,*=,/=``` |  
   | 7 | 후위연산자 | ```a++,b--``` |  

_왜 표가 안 만들어지냐;;?_  


```
* 오버플로 : 저장하고자 하는 데이터가 자료형이 저장할 수 있는 최대치보다 큰 숫자를 저장하려고 할 때 생기는 에러  

* 언더플로 : 저장하고자 하는 데이터가 자료형이 저장할 수 있는 최소치보다 작은 숫자를 저장하려고 할 때 생기는 에러  
```



### 조건문/선택문  
1. if문

```
if(조건){  
}  
```  
if 뒤에는 소괄호가 존재하고, 소괄호 내에는 true 혹은 false가 될 수 있는 조건이 필요하다.   



2. else문  

단독으로 사용할 수 없는 if문 뒤에 붙어서 사용되며, if 조건을 만족하지 않을 시 동작한다.  



3. else if 문  

if문의 조건을 만족하지 못할 때, 또 다른 조건을 추가할시 사용한다.



4. switch문  

if문과 다르게 int형 조건을 기본으로 가진다.  
   1. case문 : switch문 내에서 여러 번 사용할 수 있으며, case문 뒤에는 switch의 조건을 만족하는 숫자를 적고 ':'를 적는다. 숫자가 switch문의 조건을 만족하면 해당 case문부터 ```break;``` 명령을 만날 때까지 프로그램이 실행된다.  
   2. default문 : case문에 만족하는 조건이 없을 시 동작하는 부분을 불필요하면 생략할 수 있다. 하나의 switch문 안에 단 하나만 사용할 수 있다.  




### 반복문  

1. for문  

```
for(시작조건;실행조건;증감식){
}
```  

   > 1. 시작 조건 : 변수 1개를 선언하거나, for문 바깥에서 선언된 변수의 값을 바꿀 수 있다.  
   시작 조건은 가장 처음 단 1회만 실행된다.  
   > 2. 실행 조건 : true를 만족할 때 for문이 동작한다.  
   > 3. 증감식 : 변수의 값을 변화시킬 수 있다.  



2. 이중 for문  
: for문 내부에 for문이 존재  

   

3. while문  
: 오직 실행조건만으로 동작한다.  

```
while(동작, 조건){
}
```  


동작을 정확하게 명시하지 않으면 무한루프 현상이 나타난다.  



4. do while문  

```
do{
   동작, 내용
} while(동작, 조건);
```

* while문과의 차이점 : while문은 동작 조건을 먼저 확인하고 실행하지 말지 결정하지만, do while문은 우선 1회 동작 후, 조건을 확인하여 반복할지 말지를 결정한다.  



5. break문  
: switch문 및 반복문을 벗어나기 위한 문법이다.
break문을 만나면 그 즉시 종료한다.  



6. continue문  
: 반복문에서만 사용되는 문법으로, 반복문에서 continue문을 만나면 반복문의 조건이 있는 곳으로 돌아간다.  




### 메소드  

* 메소드는 함수와 같은 역할을 하며, 코드의 간결성을 높여준다.  
   > 1. 입력과 출력이 존재한다.  
   > 2. 입력은 매개변수 혹은 파라미터라고 부른다. 이때 매개변수로 선언된 변수들은 매소드 내에서 지역변수처럼 사용할 수 있다.  
   > 3. 출력은 리턴값이라고 부르며, 메소드가 종료된 뒤 최종으로 남는 결과 값을 뜻한다.  



* 기본구조  
   메소드 리턴 값의 자료형, 메소드 이름, 매개변수, 메소드 내용, return  



```
import java.io.*;
class Main {
	
	public static	int add(int a, int b) {
	
		int result = a+b;
	
		return result;
	}

	public static void main(String[] args) throws Exception {
		System.out.print(add(4, 6));
	}
}
```  

```public static int add ~ return result까지가 메소드에 해당하는 부분이다.```  


_메소드를 만들고 메소드 내용을 코딩하는 것을 ```메소드 정의```라고 한다._




1. ```return``` : 메소드 종료를 의미한다.  
   _"반환한다"_   
   ```
   return으로 반환될 값은 메소드를 정의할 때 명시했던 메소드 return값의 자료형과 동일한 자료형의 변수 혹은 상수만 가능하다.  



2. ```void``` : return 값에 대해 예외로 판단되는 자료형으로 어떤 값도 저장하지 않는 빈 공간을 말한다.  

  - return 값의 자료형의 void인 경우 
   : return값은 어떠한 것도 존재해서는 안 되며 , 이 경우에는 return 문구를 생략할 수 있다.  



3. ```main 메소드``` : 모든 프로그램에서 오직 하나만 존재하는 메소드이다. JAVA는 main 메소드로부터 시작되어 main 메소드의 끝고 함께 종료된다.  



4. 메소드 사용하는 방법  
: 메소드가 정의되어 있어야 한다.   
메소드 이름, 매개변수를 묶을 괄호, 매개변수 자료형에 부합하는 데이터가 필요하다. ```minus(a,5);```  
* <b>콜(call)한다</b> : 메소드를 사용하는 것 
* 메소드 앞에는 ```static```을 붙여야 한다.   



5. 오버로딩 : 메소드의 이름은 동일하게 정의하고 매개변수 혹은 리턴 값만 변경하여 정의하는 메소드 기법  
- 변수나 메소드가 너무 많거나 비슷한 동작을 하는 메소드를 여러 개 만들어야 할 경우 유용하다.  




6. ```Call By Value``` : 서로 다른 공간에 할당된 데이터이므로 다른 메소드 내부의 값을 변화시키더라도 main 메소드의 변수 값에는 전혀 영향을 끼치지 않는다.  





### 배열(Array)  

: 하나의 변수 이름으로 여러 개의 변수를 사용할 수 있게 하는 기법  
_변수 혹은 상수의 모음_
_배열에 포함된 요소들이 연속으로 할당되는 것이 특징이다_  



1. 배열의 선언  

```
import java.io.*;
class Main {
		public static void main(String[] args) throws Exception {				
			
			int [] Array = new int[10];

		}
}
```  



```int [] Array```  
   1. [] : 배열형 변수라는 뜻  
   2. new : 참조형 자료형에 메모리 공간을 할당할 때 사용한다.  
      > 참조형 자료형 : 기본형을 제외한 나머지 자료형
         _배열은 그 자체로 참조형이기 때문에 int를 써도 참조형이 됨_  
   3. "int형 변수를 10칸 저장할 수 있는 배열을 생성한다"는 뜻이다.  



2. 배열 사용하기  

```
import java.io.*;
class Main {
		public static void main(String[] args) throws Exception {
			
			int [] Array = new int[10];
			
			Array[0] = 1;
			Array[3] = 5;
			//Array[10] = 10; 잘못된 사용법입니다.
			
			System.out.println(Array[0]);
			System.out.println(Array[3]);
		}
}
```



   1. 메모리에는 순서가 0부터 시작하는 10칸의 메모리 공간이 생성된다.  
   _n칸의 배열을 생성했다면, 0번부터 n-1번까지 사용할 수 있음_  







### String  

* ```char```는 한 개의 문자만 저장이 가능하다.  
* ```String```은 여러 개의 문자를 저장한다.  



1. 배열과 String  
배열은 처음 선언할 때 전체 길이를 한정짓기 때문에 저장할 수 있는 데이터의 최대치가 정해져있다. 따라서 ```char```을 사용해서 문자를 여러 개 저장하고 싶다면, 문자의 최대 개수가 배열의 크기를 넘지 않아야 하는데, ```String```을 통해 이를 해결할 수 있다.  


   1. 문자열 : 여러 개의 문자의 묶음을 말한다.  
      " "로 감싸서 표현한다.  
   

   2. char와 String의 차이점  

```
   import java.io.*;
class Main {
        public static void main(String[] args) throws Exception {
            
            String str;
            str = "GURUM";
            
            System.out.println(str);

            char [] cArr = new char[5];
            //cArr = "GURUM"; 이렇게 사용하는 것은 불가능합니다.
        }
}
```



2. ASCII 코드  : 1Byte(8bit)로 표현할 수 있는 숫자를 각각의 문자와 매칭시킨 코드이다.  
   _Switch문의 조건에는 정수만 들어갈 수 있다. char형에 저장되는 문자가 ASCII 코드표에 의해 각각의 글자와 대응되는 숫자로 표현될 수 있기에 switch문의 조건으로 들어갈 수 있다._  


   > 1. 공백도 컴퓨터 입장에서는 하나의 문자다.  
   > 2. 젤 마지막 칸에는 NUL문자가 저장된다.  




3. 클래스와 String  

* 클래스 : 변수와 함수를 동시에 가지고 있는 사용자 정의형.
* String 자료형은 그 자체로 클래스이다.  





### 클래스와 객체  

* 클래스 : 사용자가 직접 정의하여 사용할 수 있는 자료형.  
* 객체 : '클래스'라는 자료형으로 만들어진 변수.  
> _클래스는 객체가 선언됐을 때 실체를 가지게 되며, 객체를 통해 클래스에 포함된 다양한 데이터를 다룰 수 있다._  



   1. 붕어빵 틀 없이 붕어빵이 만들어질 수 없고, 붕어빵 틀은 붕어빵을 만들지 않으면 쓸모 없는 도구가 된다.  
      = 클래스 없이 객체를 만들 수 없고, 객체를 만들지 않으면 쓸모없다.  
   2. 붕어빵 틀을 사용하기 위해 재료와 사용 메뉴얼이 필요하며, 만들 수 있는 붕어빵의 종류는 다양하다.  
      = 클래스는 멤버 변수와 멤버 메소드로 구성될 수 있으며, 객체는 동일한 틀을 가지지만 틀 안에 포함된 내용이 다룰 수 있다.  

   
* 동일한 클래스로 선언된 객체들의 형식과 규칙은 동일하지만 데이터 내용이 다를 수 있다.  




1. 멤버 : 클래스를 구성하는 요소로, 메소드와 변수로 이루어져 있다.  
 - 클래스는 멤버를 통해 내부의 데이터를 저장하거나 연산할 수 있는데, 이 때 클래스 내부의 변수를 ```멤버 변수```라고 부른다.  





```
import java.io.*;
class Main {
	public static void main(String[] args) {
		ClassExample ce;
		ce = new ClassExample();
		
		ce.mDouble = 10;
		ce.CE_Print_mDouble();
		
		ce.CE_Set_mDouble(30);
		ce.CE_Print_mDouble();
	}
}

class ClassExample {
	
	double mDouble;
	
	void CE_Print_mDouble() {
		System.out.println(mDouble);
	}
	
	void CE_Set_mDouble(double dInput) {
		mDouble = dInput;
	}
}
```

   1. 클래스는 Class Exmaple이라는 이름으로 정의되었다.  
   2. CE_Print_mDouble이라는 void형 메소드, CE_Set_mDouble이라는 void형 메소드  
   
   _멤버 변수 혹은 메소드는 갯수 제한 없이 필요한만큼 선언하여 사용할 수 있다._
    
   _심지어 변수 혹은 메소드가 존재하지 않아도 클래스를 만들 수 있다._  

   3. ClassExample 클래스를 자료형으로하고 ce라는 이름을 가진 객체가 선언되었다.  
   4. 기본형 자료형을 제외한 나머지가 모두 참조형 자료형이기 때문에 클래스로 만들어진 자료형을 ```new```로 <b>메모리 할당 과정</b>을 거쳐야 한다.  
   > C++에서는 선언만으로도 객체를 사용할 수 있지만, JAVA에서는 선언만으로는 사용할 수 없다.  
   > ```new``` 뒤에 오는 ```클래스이름()``` 부분은 <b>생성자</b>라고 한다. 객체에 new로 메모리를 할당할 때에는 꼭 생성자를 적어주어야 한다.  
   5. 클래스 내부의 멤버들은 객체를 통해 제어할 수 있다.  



   ```
   ce.mDouble = 10;
   ```

   객체 뒤에 "."을 붙이게 되면 객체 내부의 멤버 변수 및 메소드를 사용할 수 있다.  







2. 생성자 : 사용자가 객체를 생성할 때 자동으로 호출되는 메소드  

* 메소드와 생성자 비교  
-|메소드|생성자|  
|:---:|:---:|:---:|  
사용형태|return형 메소드명(파라미터1, 파라미터2)|클래스명(파라미터1,파라미터2)  
예시|void Add(double a, double b)|ClassExample(int a, int b)  


_생성자는 return형을 사용하지 않으며 클래스와 동일한 이름을 가져야 한다._  



* 기본 생성자 : 매개변수가 존재하지 않는 생성자  
   > 매개변수를 포함한 생성자 또한 만들 수 있다.
   "클래스 안에 매개변수가 들어간 생성자만 정의했다면, 객체에 메모리를 할당할 때 생성자에 포함된 매개변수를 잊지말고 입력해야 한다."  


* 생성자는 보통 멤버 변수들의 초기화 및 객체의 복사와 같은 역할로 사용된다.  




3. 접근제한자 : 멤버 변수 및 메소드를 선언할 때 사용한다.  


   1. 자료 제한 범위  
      - public : 제한 없음  
      - protected : 자식 클래스에게는 public, 그 외에는 private  
      - NOT USE : 같은 패키지에서는 public, 그 외에는 private  
      - private : 본인 객체 내에서만 사용 가능  


```
import java.io.*;
class Main {
	public static void main(String[] args) {
		ClassExample ce;
		ce = new ClassExample();
		
		ce.mDouble = 10;	// 오류 발생
		ce.CE_Print_mDouble();
		
		ce.CE_Set_mDouble(30);
		ce.CE_Print_mDouble();
	}
}

class ClassExample {
	
	private double mDouble;
	
	public void CE_Print_mDouble() {
		System.out.println(mDouble);
	}
	
	public void CE_Set_mDouble(double dInput) {
		mDouble = dInput;
	}
	
}
```  


   - private 접근제한자는 객체 자기 자신 안에서만 사용할 수 있기 때문에 7번째 줄처럼 객체의 바깥에서 멤버에 직접 접근을 시도하면 오류가 발생한다. 따라서 public으로 선언된 멤버를 활용해야 한다.  





4. static에 대하여  

main 메소드에서는 무조건 ```static```이 붙어야 한다. static은 메소드 혹은 변수에 붙어 사용할 수 있다. <b>만약 클래스 안의 멤버에 static이 붙으면 그 멤버는 클래스의 객체를 선언하지 않고 바로 콜해서 사용할 수 있다.</b>   


   > main 메소드에 ```static```이 붙어야 하는 이유는 main 메소드가 프로그램이 처음 시작되는 메소드이기 때문에 main 메소드보다 빨리 실행될 수 있는 코드가 없기 때문에 static을 사용하지 않으면 main 메소드의 메모리를 할당해줄 부분이 존재하지 않기 때문에, 프로그램의 시작과 함께 main 메소드의 메모리를 할당해야 한다.  








### 데이터 입출력  

* 콘솔 : 대표적인 CLI 개발 환경으로 글자를 이용한 입출력 환경을 뜻한다. 


1. 키보드 데이터 입력받기 ```Scanner```   

 

```
import java.io.*;
import java.util.Scanner;	// Scanner 사용시 명시 필수!

class Main {
	public static void main(String[] args) {
		int iVal;
		double dVal;		
		
		Scanner scanner = new Scanner(System.in);
		
		System.out.print("정수를 입력해주세요 : ");
		iVal = scanner.nextInt();				
		System.out.println("입력 정수 : " + iVal);
		
		System.out.print("실수를 입력해주세요 : ");
		dVal = scanner.nextDouble();				
		System.out.println("입력 실수 : " + dVal);
	}
}
```  


   1. ```Scanner```클래스를 사용하기 위해서는 ```import java.util.Scanner; ```를 꼭 명시해줘야 한다.   
   2. scanner 객체에 메모리가 할당되고 나면 ```nextInt()```메소드 혹은 ```nextDouble()```메소드 등을 사용해서 사용자가 입력하는 숫자를 본인이 원하는 변수에 저장할 수 있다.  




2. 키보드 데이터 입력받기 : ```BufferedReader```  



```
import java.io.*;

class Main {
    public static void main(String[] args) throws Exception {
        
    	String sVal;
    	
		// BufferedReader 초기화
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        
        System.out.print("문자열을 입력해주세요 : ");
        sVal = br.readLine();
        System.out.println("입력 문자열 : " + sVal);
        br.close();
    }
}
```  


   1. 

















