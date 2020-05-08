# Java 정리 🍎🍊🍉

## 초창기 시절에 JAVA 언어의 단점
  
 1. 기존 C/C++에 비해서 속도가 굉장히 느리다.
 2. 리소스( 메모리,CPU )를 많이 사용한다. 

## 현재 JAVA 언어의 장점

 1. 객체 지향 언어로 기능을 부품화할 수 있다. -> 하나하나를 객체를 합쳐 큰 프로그램을 만들 수 있다는 것  
 2. JRE를 이용해서 운영체제로부터 자유롭다. -> 윈도우에서 코딩을 했지만 -> 리눅스용 JRE를 설치하면 자유롭게 할 수 있다는 점 
 3. 웹 및 모바일 프로그래밍이 쉽다. 
 4. GC를 통한 자동 메모리 관리를 지원한다.  Garbage colllector를 통해
 5. 실행속도가 많이 개선되어 빨라졌다. 




## 가비지 컬렉터 (Gabage Collector) 

	- 프로그램 실행에 필요한 메모리를 Gabage Collector 가 자동으로 관리한다. 
	
      
  ##         C 계열 프로그램                                        Java 프로그램

  개발자가 직접 메모리를 관리해야함           개발자가 메모리에 접근할 수 없음.
 만약 메모리관리를 잘못할 경우              따라서 개발자는 메모리관리를 할 수 없고 
 메모리 누수가 발생하고                     가비지 컬렉터가 불필요한 메모리를 회수해서 
 타 프로그램 동작이 멈출 수 있다.                    메모리를 최적화 함 


## 기본자료형과 객체자료형 

 기본자료형은 데이터가 변수에 직접 저장되고, 객체 자료형은 객체 메모리 주소가 변수에 저장된다.
 C 계열에서는 포인터라고 하고, Java에서는 레퍼런스라고 한다. 





## 객체란?

 세상에 존재하는 모는 것을 뜻하며, 프로그래밍에서 속성과 기능을 가지는 프로그램 단위이다.

객체 (인간세상)    ㅜ                                                     객체 (프로그램)
   ex) 사람  속성: 키, 몸무게 , 기능: 의사                        사칙연산 프로그램 속성 : *,+,-,/ 
        체중계 속성: 바늘, 눈금 기능: 몸무게측정                기능: 연산기능 


## 클래스란? 
  
  객체를 생성하기 위한 틀로 모든 객체는 클래스로부터 나온다. 
     
    선수용 자전거, 사람용 자전거, SUV,등등 객체가 어떤걸 쓰느냐에 따라 달라질 수 있다. 
    붕어빵 기계 틀  
    객체를 하나만 만든다고 하더라도 클래스가 필요하다.
    클래스만 만들고 객체를 뽑아내고 그럼 그건 메모리에 탑제된다.  


## 클래스 구성요소  (자전거)

   속성 (멤버변수) = 인장, 핸들, 바구니, 기어, 페달
   기능 (메서드) = 기어변속, 가속, 브레이크

## 가비지 컬렉터 

가비지 컬렉터가 쓱 가져간다 -> 떠돌아다니는 변수나 객체를 처리하는 역할 ( 누구도 참조하지않고, 연결되어 있지 않은 것들은 처리하는 역할 )


## 클래스 제작과 객체 생성 

클래스는 멤버변수 (속성) , 메서드(기능) , 생성자 등으로 구성된다. 

Void ->반환값이 없다. 
Public string run() -> 반환값이 string이다 

## 생성자

클래스이름과 동일한 메서드 
반환형이 없다. 
생성할때 (가장 먼저 !!!) 필요한 기술을 사용하면 된다. 


## 메서드 

메서드 선언부 , 정의부로 나눌 수 있다.

접근자 반환형 메서드이름  메개변수
Public   void     getInfo      ()      {
   
      System.out.println( " i  = " + i); 

}

## 중복 메서드 ( overloading)

이름은 같고, 매개변수의 개수 또는 타입이 다른 메서드를 만들 수 있다. 

 Public void getInfo(){

System.out.println(" ---getInfo - I --");

}
Public void getInfo(String str, int ins){

System.out.println(" ---getInfo - II --");

}
  


## 메모리에서 객체 생성(동적 생성)
  
객체는 메모리에서 동적으로 생성되며, 객체가 더 이상 필요 없게되면 GC에 의해서 제거된다.

ChildClass child = new ChildClass();

여기서 child 는 레퍼런스 

-> 생성된 객체의 주소를 변수에 저장하는 것을 레퍼런스라고 한다. 

## Null과 NullPointException

레퍼런스에 null 저장되면 객체의 연결이 끊기며, 더 이상 객체를 이용할 수 없다.
회수해가면 없어진다.

## 디폴트 생성자 
 
객체가 생성될 때 가장 먼저 호출되는 생성자로, 만약 개발자가 명시하지 않아도 컴파일 시점에 자동 생성된다.
사용자정의 생성자

디폴트 생성자가 없더라도 컴파일러가 자동으로 생성한다. 
 

## 소멸자 

객체가 GC에 의해서 메모리에서 제거 될 때 finalize() 메서드가 호출된다. 
System.gc() ; // 이걸 사용한다고 해서 GC가 바로 작동하는 것이 아니라!(GC바쁨) ,가급적 빨리 작동하도록 요청하는 것이다.
                    java는 기본적으로 메모리를 개발자가 직접관리하지않으므로 일반적으로 System.gc(); 를 사용하는 경우는 드물다



## this 키워드 

현재 객체를 가리킬 때 this를 사용한다. 

  this.x = x; //나자신의 객체를 가리킴 -> 전역변수 , 클래스에 있는 개체를 말한다. !!!!!
  this.y = y;

 - 객체 지향 프로그래밍이 뭐냐?
	1. 프로그램을 수 많은 객체라는 기본 단위로 나누고, 이 객체들의 상호작용으로 프로그램을 구성하는 방식
	2. 로직은 상태(state)와 행위( behave)로 이루어진 객체로 만드는 것이다. 
	3. 레고 블록처럼 객체를 조립해서 하나의 프로그램을 만드는 것 
	4. 코드의 재사용성을 증가시키는 목적
	5. 유지보수를 감소시키는 장점
	6. 강한 응집력, 약한 결합력을 지향 
	
-> 재사용성을 증가시키는 목적 

## 객체지향 프로그래밍 특징
	1. 캡슐화 
	-> 세부 구현을 외부로 드러나지 않도록 특정 클래스 내부로 감추는 것,  접근 제어 지시자를 통해 외부에서 접근을 제어한다. 
  2.   상속
       ->자식 클래스가 부모 클래스의 특성과 기능을 그대로 물려받는 것을 말한다. 자식클래스에서 재정의를 통해 부모클래스의 메소드를 사용할 수 있다.
  3.   다형성  ( overloading )
       -> 하나의 메소드, 클래스가 상황에 따라 다른 의미로 해석될 수 있다. 
   
  # list , arraylist, linkedlist 
 
## List
   - 데이터와 인덱스값이 있다. 
   - Java에서는 list는 배열의 크기가 fix되어 있다.
   - 순서가 있는 엘리먼트들의 모임이다. 빈 엘리먼트는 허용되지 않는다. 그리고 중복된 데이터를 허용한다. 
  

 
## Arraylist
   - 데이터가 추가하는데로 늘어나는 장점 O(1)
   - 배열방이 다 차면 기존 사이즈의 2배를 선언하고 기존 값을 복사한다. -> Doubling이라고 함.
   - 인덱스를 이용하여 데이터를 가져오기
 
## Linkedlist 
  -  Arraylist 와는 다르게 엘리먼트와 엘리먼트 간의 연결(link)을 이용해서 리스트를 구현한 것을 의미한다. 
 - linkedlist는 그 위치가 흩어져 있기 때문에 서로 연결되어 있어야 한다. 
 - 리스트는 노드(엘리먼트)들의 모임이다. 그래서 내부적으로 노드를 갖고 있어야한다. 
 - 데이터의 추가/삭제가 빈번하다면 효과적

    

## 클래스 
 - 객체를 만드는 기능을 한다. 
 - 붕어빵틀 의미
 - 여러가지 필드와 메소드를 가진다. 
 -  JVM 시작 시 RunTimeData Area 의 Method (Static)   
    JVM은 자바 가상 버신의 약자로 자바와 OS사이의 중개자 역할을 하며, 메모리관리 ,가비지컬렉션을 수행합니다. 스택기반의 가상머신 
 - 메모리를 효율적으로 관리하기 위하여 사용 


	- 필드 = 속성 = 상태 = 멤버변수 , JVM의 Method(Static) Area에 해당

 생성자도 overloading과 같다 

## Instance 생성 

	- 인스턴스란 설계도를 바탕으로 소프트웨서 세계에 구현된 구체적인 실체 
	- 객체에 포함된다고 할 수 있다. 
	- Animal cat // 객체 
	cat = new Animal (); //cat은 Animal 클래스의 '인스턴스'
	
## 은닉화  -> 캡슐화 
   - 클래스의 Field는 Private로 접근 제어지시자로 지정한 뒤 Getter, Setter 를 통해 Filed의 값을 변경, 호출한다. 
 
  - Getter : 값을 호출, 
     Setter : 값을 변경 

## 접근 제어 지시자 


## Builder 패턴
 - 생성자에 들어갈 매개변수를 차례대로 받아들이고 모든 매개변수를 받은 뒤에 이 변수들을 통합하여 한번에 사용한다.
 - 데이터의 순서에 상관없이 객체를 만든다. 
 - 사용자가 봤을 때 명시적이고 명확하게 이해할 수 있어야한다. 
 - 불필요한 생성자를 만들지 않고 객체를 만든다. 


                  





## 인터페이스
	- 자바에서 클래스들이 구현해야하는 동작을 지정하는데 사용되는 추상형
   -  규약, 규제 
   - 인터페이스도 상속이 가능하고, 클래스와 달리 다중구현이 가능하다 

Java 8 에서는 디폴드 메소드 추가되면서 이전에 개발한 구현클래스를 그대로 사용하고, 변경하지 않으면서 새롭게 개발하는 클래스는 디폴트 메소드를 이용해 새로운 기능을 개발할 수 있다. 

## Extends 와 implements (상속)
Extends 는 상속의 대표적인 형태이다. 
 -> 부모의 메소드를 그래도 사용할 수 있으며 오버라이딩 할 필요 없이 부모에 구현되어있는 것을 직접 사용 가능하다. 
Implements (인터페이스)는 다중상속을 대신해준다. 
 -> 부모의 메소드를 반드시 오버라이딩해줘야 한다는 것 

## Generic (제네릭)
   - 클래스 내부에서 사용할 데이터타입을 외부에서 지정하는 기법 
   - 다양한 타입의 객체를 다루는 메소드나 , 컬렉션 클래스에서 컴파일시 타입체크를 해주는 기능이다. 
	- 타입 안정성을 제공한다. 
	- 타입체크와 형변환을 생략할 수 있으므로 코드가 간결해진다. 
	- 중복제거 가능 
	- 컴파일 단계에서 오류를 찾을 수 있다.

## String , StringBuffer ,StringBuilder

위에서 보는바와 같이 생성된 클래스의 주소값이 다른 것을 볼 수 있다. String은 새로운 값을 할당할 때마다 새로 생성되기 때문이다. 이와 달리 StringBuffer는 값은 memory에 append하는 방식으로 클래스를 직접생성하지 않는다. 논리적으로 따져보면 클래스가 생성될 때 method들과 variable도 같이 생성되는데, StringBuffer는 이런 시간을 사용하지 않는다.

StringBuilder와 StringBuffer를 테스트 해보자. 아래의 결과를 보면 다른 값이 나온 것을 볼 수 있다. StringBuilder의 값이 더 작은 것을 볼 수 있는데 이는 쓰레드들이 동시에 StringBuilder클래스에 접근할 수 있기 때문에 일어난 결과다. 이와 달리 StringBuffer는 multi thread환경에서 다른 값을 변경하지 못하도록 하므로 web이나 소켓환경과 같이 비동기로 동작하는 경우가 많을 때는 StringBuffer를 사용하는 것이 안전할 것이다.


출처 : https://novemberde.github.io/2017/04/15/String_0.html

## Exception(예외)
   - 오류가 발생하지 않는 프로그램은 없다. 
   - 기능이 많아질수록 오류가 발생할 확률도 높아진다. 
	- 프로그램을 만든 개발자가 상정한 정상적인 처리에서 벗어나는 경우를 처리하기 위한 방법

## Annotation(어노테이션)
	- JAVA5 에서 추가된 문법 
	- JAVA코드에 마치 주석처럼 달아 특수한 의미를 부여한다. 
	- Compile Time, Run Time시에 해석될 수 있다. 
	- 자바, Spring이 제공해주는 것도 있고, 사용자가 직접 만들 수도 있다. 

				
				



