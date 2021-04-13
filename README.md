# Java 정리 🍎🍊🍉 (인프런 강의 + 공부하며 끄적이기! :> ) 

## 초창기 시절에 JAVA 언어의 단점
  
 1. 기존 C/C++에 비해서 속도가 굉장히 느리다.
 2. 리소스( 메모리,CPU )를 많이 사용한다. 

## 현재 JAVA 언어의 장점

 1. 객체 지향 언어로 기능을 부품화할 수 있다. -> 하나하나를 객체를 합쳐 큰 프로그램을 만들 수 있다는 것  
 2. JRE를 이용해서 운영체제로부터 자유롭다. -> 윈도우에서 코딩을 했지만 -> 리눅스용 JRE를 설치하면 자유롭게 할 수 있다는 점 
 3. 웹 및 모바일 프로그래밍이 쉽다. 
 4. GC를 통한 자동 메모리 관리를 지원한다.  Garbage colllector를 통해
 5. 실행속도가 많이 개선되어 빨라졌다. 

## OOP(Object-Oriented Programming, 객체 지향 프로그래밍)
  
  프로그램을 수 많은 객체라는 기본 단위로 나누고 이 객체들의 상호 작용으로 프로그램을 서술하는 방식
  객체들을 데이터 묶음 뿐만 아니라 하나의 역할을 수행하는 메소드와 데이터의 묶음
  큰 문제를 작게 쪼개는 것이 아니라, 먼저 작은 문제들을 해결할 수 있는 객체들로 만든 뒤, 이 객체들을 조합해서 큰 문제를 해결하난 상향식(Buttom up)   해결법 도입
  
## 캡슐화(Encapsulation)
  
  프로그램의 세부 구현을 외부로 드러나지 않도록 특정 모듈(클래스) 내부로 감추는 것이다.
  접근 제어 지시자를 통해 외부에서 접근을 제어한다.
  
## 상속(Inheritance)

 자식 클래스가 부모 클래스의 특성과 기능을 그대로 물려받는 것을 말한다.
 재정의를 통해 자식 클래스에서 상속받은 기능만들 재 정의해 사용이 가능하다.
 
 ## Implements(인터페이스 구현)
implements를 통해 부모클래스에서 선언한 변수/메소드를 자식클래스에서 재정의(오버라이딩)를 통해 인터페이스를 구현하여 상속받을 수 있다. 
여기서 잠시 인터페이스와 클래스의 차이점을 간단히 보면, 인터페이스는 메소드를 구현하지않고 정의만 내리며
이 인터페이스를 상속받은 클래스에서 해당 인터페이스에서 정의된 메소드를 구현하는 것이라 생각하면 된다.

따라서, extends는 클래스를 확장하는 것이며 implements는 인터페이스를 구현하는 것이다.

public class ChildClass implements FatherClass, MotherClass{

}


위와 같은 형태로 implements는 다중상속이 가능하게 해준다.
출처 : https://gangnam-americano.tistory.com/23



## 다형성 
 
 백준을 풀다보면 다형성의 이유로  static Queue<Point> q = new LinkedList<>();  이렇게 되어있는 경우가 종종있다. 
	
 다형성이란 상위클래스 타입 변수에 여러개의 하위클래스의 객체를 참조할 수 있도로 하는 것을 이야기한다.  ,하나의 변수, 함수 
 즉 같은 타입이지만 오른쪽에 실제 런타임중에 new되는 객체(하위클래스)의 메소드가 실행되어 동일한 메소드가 다양한 형태로 표출한다는 것.   
	
	장점
	    1. 여러 타입의 객체를 하나의 타입으로 관리하니 유지보수가 좋다. 
	        (변경사항 발생시 다형성으로 구현하지 않았을 떄의 절반이상 코딩양이 줄어든다. )
	    2. 메소드의 매개변수(인자)로 상위 클래스 , 추상클래스, 인터페이스 등이 온다면
	       그 하위클래스, 인터페이스를 구현한 클래스등이 인자로 들어 갈 수 있어 좀 더 
	       유연한 프로그래밍을 할 수 있다. 
	    3. 확장성이 좋은 코드를 작성할 수 있고, 결합도가 강하지 않은 프로그래밍을 할 수 있다. 
	    
	    출처 : http://ojc.asia/bbs/board.php?bo_table=LecCsharp&wr_id=225

### polymorphism 다형성
 다형성의 사전적 정의는 같은 종의 생물이지만 모습이나 특징이 고유한 특징이 다양한 성질을 의미한다.
 객체지향개념의 중요한 특징 중 하나이다.
 여러 가지 형태를 가질 수 있는 능력을 의미한다.
 자바에서는 한 타입의 참조변수로 여러 타입의 객체를 참조할 수 있도록 함을 구현하는데 사용한다.
 좀 더 구체적으로는 조상 클래스 타입의 참조변수로 자손클래스의 인스턴스를 참조할 수 있도록 하였다.
 어떤 클래스를 인스턴스화 시킬 때, 변수를 담는 데이터 타입은 그 클래스가 될 수도 있고 그 클래스의 부모 클래스가 될 수도 있다.
 
 다형성이란 같은 자료형에 여러 가지 객체를 대입하여 다양한 결과를 얻어내는 성질을 의미한다.
 하나의 타입으로 다양한 실행 결과를 얻을 수 있으며 객체를 부품화하여 유지 보수를 용이하게 한다.

### 다형성 구현 방법
클래스의 상속이나 인터페이스를 구현하는 자식 클래스에서 메서드를 재정의(오버라이딩)하고 자식 클래스를 부모 타입으로 업캐스팅한다.
그리고 부모 타입의 객체에서 자식 멤버를 참조하여 다형성을 구현한다.

  상속, 구현
 자식 클래스에서 메소드 재정의(오버라이딩)
 업캐스팅
 부모 클래스(인터페이스)에서 부모 객체로 자식 멤버 사용, 하나의 타입으로 다양한 결과를 얻음
 참고
 https://asfirstalways.tistory.com/168
 https://m.blog.naver.com/PostView.nhn?blogId=heartflow89&logNo=220979244668&proxyReferer=https%3A%2F%2Fwww.google.com%2F
 https://devbox.tistory.com/entry/Java-%EB%8B%A4%ED%98%95%EC%84%B1

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


## 자바에서 포인터가 없는 이유 


##   정수형 < 실수형 
 byte < short < int < long          < float < double 
 : 타입크기는 표현범위로 정하는 것 
큰수, 작은 수 효율적인 저장이 가능하기 때문에 
long < float 이 된다. 

####
while(1) {} -> 안되고 
while(true)로 정확하게 줘야한다.

## 양의 정수 이런거 없다. 
unsigned 가 없어 
signed 형만 있다. 


10. 묵시적 형변환은 데이터 손실 발생 
명시적 형변호는 데이터손실 발생 가능 
양수 전용으로만 하는 것 
11. long형인 8바이트형 값이 되는것 
long a = 10

double d = 2 
int를 double에 ! 
그러면 2.0 이 들어가게 된다. 


연산은 
동일한 데이터타입으로 할 수 있다.

크기,  각 데이터의 의미가 같아ㅏ야지만 가능  

long k = i*j

10억 * 3 
int * int = int -> (long) 바꿔도 
오버플로우가 됨 
연산결과가 long형이 될 수 있도록 만들어야함 

i가 long * int -> long형이 되서 
long으로 변환됨 

데이터타입 잘 선언됨 
==================

if, switch - case / for while do while 

syntex정리 



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

### Old GC

#### Serial GC
  절대 사용하면 안 되는 방식이다.
  CPU 코어가 1개만 있을 때 사용하기 위해 만든 방식이다.
  애플리케이션의 성능이 많이 떨어진다.
  적은 메모리와 CPU 코어 개수가 적을 때 적합한 방식이다.
  GC를 처리하는 스레드가 하나다.
  Old 영역의 GC는 Mark-Sweep-Compact 알고리즘을 사용한다.
  Old 영역에 살아 있는 객체를 식별(Mark)한다.
  Heap의 앞 부분부터 확인하여 살아 있는 것만 남긴다.(Sweep)
  각 객체들이 연속되게 쌓이도록 Heap의 가장 앞 부분부터 채워서 객체가 존재하는 부분과 객체가 없는 부분으로   나눈다.(Compaction)

#### Parallel GC
  GC를 처리하는 쓰레드가 여러 개이다.
  Serial GC보다 빠르게 객체를 처리할 수 있다.
  메모리가 충분하고 코어의 개수가 많을 때 유리하다.
  
 #### Parallel Old GC(Parallel Compacting GC)
Old 영역의 GC는 Mark-Summary-Compaction 단계를 거친다.
Summary 단계는 앞서 GC를 수행한 영역에 대해서 별도로 살아 있는 객체를 식별한다.
Mark-Sweep-Compaction 알고리즘의 Sweep 단계와 다르다.
#### Concurrent Mark & Sweep GC(CMS)
Stop-the-world 시간이 매우 짧다.
모든 애플리케이션의 응답 속도가 매우 중요할 때 CMS GC를 사용한다.
Low Latency GC라고도 한다.
다른 GC보다 메모리와 CPU를 더 많이 사용한다.
Compaction 단계가 기본적으로 제공되지 않는다.
초기 Initial Mark 단계에서는 클래스 로더에서 가장 가까운 객체 중 살아있는 객체만 찾는 것으로 끝난다. 멈추는 시간은 매우 짧다.
Current Mark 단계에서는 살아있다고 확인한 객체에서 참조하고 있는 객체들을 따라가면서 확인한다. 다른 스레드가 실행 중인 상태에서 동시에 진행된다.
Remark 단계에서는 Concurrent Mark 단계에서 새로 추가되거나 참조가 끊긴 객체를 확인한다.
Concurrent Sweep 단계에서는 쓰레기를 정리하는 작업을 실행한다. 다른 스레드가 실행되고 있는 상황에서 진행한다.
#### G1(Garbage First) GC
가장 성능이 빠르다.
아직 안정화 단계이다.
## 클래스 제작과 객체 생성 

클래스는 멤버변수 (속성) , 메서드(기능) , 생성자 등으로 구성된다. 

Void ->반환값이 없다. 
Public string run() -> 반환값이 string이다 

## 생성자

클래스이름과 동일한 메서드 
반환형이 없다. 
생성할때 (가장 먼저 !!!) 필요한 기술을 사용하면 된다.

## 쇼트서킷(Short-circuit)

논리합의 경우 둘 중 하나면 참이다.
따라서 왼쪽항이 참이면 

오른쪽항은 검사하지 않아도
논리합의 전체 결과는 참이다
하지만 논리곱에서는 
왼쪽항이 참인 경우에만

오른쪽항의 연산을 수행한다.
반대로 왼쪽항이 거짓이라면 
오른쪽항을 검사하지 않아도

전체결과는 거짓이 된다.
이 같은 특징으로 
논리연산자와 조합된 다른 연산식이나
조건식이 생략되는 경우를 쇼트서킷이라 한다.
불필요한 연산이 줄어들면 
프로그램의 효율이 그만큼 높아진다.
논리 연산은 무조건 왼쪽부터 시작

## 자바 클래스의 기본 구조

 ### 패키지
  - 자바 클래스들을 같은 성격으로 묶어서 관리하는 일종의 디렉터리 개념이다. 역 도메인(Reverse Domain) 방식으로 이름을 부여한다.
 
 ### 클래스
  - 자바 프로그램은 기본적으로 클래스를 만드는 것에서부터 시작한다. 클래스는 자바 프로그램의 기본 단위이며, 프로그램 실행을 위한 main() 메서드를 반드시 클래스에 포함해야 하는 것으 아니다.
 ### 인스턴스
 - 객체지향의 개념에 따라 클래스는 바로 사용할 수 없고, 인스턴스로 사용해야 한다. main() 메서드에서는 클래스의 인스턴스를 만들고, 인스턴스를 이용하여 메서드 호출 등 필요한 작업을 처리한다.
 ### 참조 변수
  - 자바 클래스의 인스턴스 참조를 위한 변수이다. 구조는 일반적인 변수와 유사하지만, 참조 변수에는 데이터가 없고 클래스 인스턴스를 가리킨다.


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
   - 참고로, Arraylist를 정렬할시에는 
  
            Collections.sort(arrayLists[i]); // arraylist를 정렬할때에 사용하는 메소드
        
	
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

## StringTokenizer
  긴 문자열을 지정된 구분자를 기준으로 문자열을 슬라이싱하는데 사용됨.
  100,200,300,400 의 문자열을, 구분자를 기준으로 슬라이싱하게 되면 4개의 문자열을 획득할 수 있다. 
  StringTokenizer의 경우 단 한개의 구분자를 사용해야 한다는 단점이 있으므로 복잡한형태의 구분자로 문자열을 나누어야할때는
  
 - StringTokenizer(String str, String delim) : 문자열 지정된 구분자로 나누는 Stringtokenizer를 생성한다. 
 - StringTokenizer(String str, String delim , boolean retunDelims)  : 구분자도 토큰으로 간주 
 - int countTokens()  : 전체 토큰의 수를 반환 
 - boolean hasMoreTokens() : 토큰이 남아있는지 알려 줌 
 - String nextToken() : 다음 토큰을 반환한다. 
  

## Exception(예외)
   - 오류가 발생하지 않는 프로그램은 없다. 
   - 기능이 많아질수록 오류가 발생할 확률도 높아진다. 
	- 프로그램을 만든 개발자가 상정한 정상적인 처리에서 벗어나는 경우를 처리하기 위한 방법

## Annotation(어노테이션)
	- JAVA5 에서 추가된 문법 
	- JAVA코드에 마치 주석처럼 달아 특수한 의미를 부여한다. 
	- Compile Time, Run Time시에 해석될 수 있다. 
	- 자바, Spring이 제공해주는 것도 있고, 사용자가 직접 만들 수도 있다. 

## Token(토큰)
      - Statelss방식이다. 상태유지를 하지 않는다.
      - 사용자의 인증 정보를 서버나 세션에 담아두지 않는다.
      - 세션이 존재하지 않으니 로그인 되어있는지 안 되어있는지 신경도 쓰지 않으면서 서버를 손쉽게 확장할 수 있다.
      - 모바일 애플리케션에 적합하다.
      - 인증 정보를 다른 애플리케이션에 전달할 수 있다.(OAuth)
      - 서버 기반 인증의 문제점 - 세션, 확정성, CORS의 문제점을 보완할 수 있다.				
				

## 운영체제 (다음에 따로 만들 예정 ! )

## 프로세스(Process)
로더에 의해 주기억 장치에 상주된 프로그램이 CPU에 의해서 처리되는 상태

CPU에 의해 현재 실행되고 있는 프로그램이다.

PCB(Process Control Block, 프로세스 제어 블록)의 존재로서 명시되는 것이다.

프로세서(Processor)가 할당되는 개체로서, 디스패치(Dispatch)가 가능한 단위이다.

지정된 결과를 얻기 위한 일련의 계통적 동작이다.

목적 또는 결과에 따라 발생하는 사건들의 과정이다.

비동기적 행위를 일으키는 주체이다.

프로시저가 활동 중인 상태를 말한다.

실행중인 프로시저의 제어 궤적이다.

CPU가 할당되는 실체이다.

운영체제가 관리하는 최소 단위의 작업 프로그램이다.

## Compiler
 - 각 소스코드 파일을 오브젝트파일로 변환시켜주는 역할을 한다.

## Loader(로더)
 - 목적 프로그램(기계어 파일)을 실행 가능한 파일로 변환하기 위해 컴퓨터의 주 기억 장소를 할당(Allocation)하거나, 여러개의 목적      프로그램을 연계 편집하여 CPU가 처리할 수 있는 프로그램으로 변환시킨다.
 - 프로그램을 실행하기 위하여 프로그램을 보조 기억 장치로부터 컴퓨터의 주 기억 장치에 올려 놓는 작업을 수행
 - 목적 프로그램들 끼지 연결(Linking)시키거나, 주 기억 장치를 재배치(Relocation)하는 증 포괄적인 작업을 수행

  할당(Allocation) -> 연결(Linking) -> 재배치(Relocation) -> 적재(Loading) 순으로 진행

## Linker
   - 모든 오브젝트 파일들을 하나의 오브젝트 파일로 합친다.
   
## JVM (자바 가상 머신)
 - Java Application을 Class Loader를 통해 읽어 들여 Java API와 함께 실행하는 것이다.
 - Java ByteCode를 실행할 수 있는 주체이다.
 - 인터프리터나 JIT 컴파일 방식으로 다른 컴퓨터 위에서 Java ByteCode를 실행할 수 있도록 구현한다.
 - Java ByteCode는 플랫폼에 독립적이다.
 - 모든 JVM은 JVM 규격에 정의된 대로 Java ByteCode를 실행한다.
 - 이론적으로 모든 자바 프로그램은 CPU나 운영체제의 종류와 무관하게 동작할 것을 보장한다.
 
 http://pigbrain.github.io/java/2016/04/04/Java8_on_Java
 
 ## if문         ## switch문
 
  if , if - else , if - else if else
  
  총 3가지로 되어있다.
  
  정수로 교묘하게 할 경우 
  switch 문 이 if문 보다 성능이 낫다고 함 
  그래서, switch 문을 잘 활용하면 좋다. ( 자주 사용하는 습관을 들이도록 ! )
  
  switch 문 안에 int , byte, short, char, String까지 되지만(String도 자바 1.8이되면서,,? 사실 이건 잘기억안남,,), double형은 안됨

 
 ## 자바의 정렬 
 ### 1. Comparable 과 Comparator란?

1. Comparable 인터페이스
- 정의: 정렬 수행시 **기본적으로 적용되는 정렬 기준이 되는 메서드를 정의해 놓는 인터페이스**이다.
- 사용법: **Comparable 인터페이스를 implements 한 뒤, 내부에 있는 compareTo 메서드를 원하는 정렬 기준대로 구현**하여 사용할 수 있다.
- 패키지:  **java.lang.Comparable**
- 자바에서 제공되는 정렬이 가능한 클래스들은 모두 Comparable 인터페이스를 구현하고 있으며, 정렬시에 Comparable의 구현 내용에 맞춰 정렬이 수행된다.

예를 들어 Integer, Double 등의 클래스의 경우 비 내림차순(오름차순과 유사), String 클래스의 경우 사전순으로 정렬되게 구현되어 있다. 

2. Comparator 클래스

- 정의 : 정렬 가능한 클래스 (=Comparable이 구현된 클래스)들의 **기본 정렬 기준과는 다른 방식으로 정렬하고 싶을 때 사용하는 클래스**이다.
- 사용법: **Comparator 클래스를 생성하여, 내부에 compare 메서드를 원하는 정렬 기준대로** 구현하여 사용할 수 있다.
- 패키지: **java.util.Comparator**
- 주로 익명클래스(new Comparator() {...})로 사용되며, 기본적으로 오름차순이 정렬 기준인 것을 내림차순으로 정렬하는 등의 용도로 사용된다.

[비교]

### Clone() : clone 원본 객체의 필드값과 동일한 값을 가지는 새로운 객체를 생성
- 복제이유: 원본객체를 안전하게 보호하기 위해서
-  cloneable 인터페이스를 구현하지 않으면 clone()메소드를 호출할 때 CloneNotSupportedException예외가 발생
-  try-catch 구문 필요
- 얕은복제(this clone)와 깊은복제(deep clone)가있음

출처: https://jyosssss.tistory.com/78 [개미는 뜐뜐]
출처: [https://m.blog.naver.com/occidere/220918234464](https://m.blog.naver.com/occidere/220918234464)
