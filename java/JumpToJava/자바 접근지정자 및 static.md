# 자바 - 콘솔입출력, 접근지정자, static키워드  
* 인터페이스 보충설명
    * 추상 클래스 정의 시 class 앞에 abstract 를 붙힌다.
    * 추상 메소드 정의 시 접근지정자 뒤에 abstract를 붙힌다
    * 클래스처럼 구현부가 있는 메소드를 가질 수도 있다

* 콘솔 입출력
    * System.in은 InputStream타입의 객체이다
    * InputStream 의 인스턴스 in 을 생성하자
        * in.read() 메소드는 한 바이트만을 읽는다 예) 'abc'를 입력하면 'a'만 읽는다
    * 스트림 == 데이터... 데이터의 흐름을 스트림이라고 한다.
    * 문자를 바이트 단위로 읽어 아스키코드값으로 저장하는 대신 문자로 입력스트림 읽는법
        * InputStreamReader 사용. 객체를 생성할 때는 생성자의 입력으로 InputStream의 객체가 필요하다.
        * read()메소드 사용
    * 고정된 길이만큼만의 입력 스트림을 읽지 않고 사용자가 엔터키를 입력하기 전까지의 입력을 전부 받아들이는 법
        * BufferedReader 사용
        * readLine() 메소드 사용
  
 >InputStream - byte  
 InputStreamReader - character  
 BufferedReader - String  

* 패키지
    * 패키지는 비슷한 성격의 자바 클래스들을 모아 넣는 자바의 디렉토리이다
    * EungYongPark이라는 클래스의 패키지는 jump2java.house.person으로 HousePark의 패키지인 jump2java.house와 다르다
    * default 접근 지정자로 지정된 멤버는 같은 패키지의 클래스에서 접근이 가능하다.

* static
    * 모든 객체와 클래스가 공유하는 멤버
    * final static -> 변수의 값을 변경할 수 없게 하는 키워드이다
    * 클래스를 통해 호출 할 수 있다

* 싱글톤 패턴
    * 싱글톤은 단 하나의 객체만을 생성하게 강제하는 패턴이다. 
    * 즉 클래스를 통해 생성할 수 있는 객체는 한 개만 되도록 만드는 것이 싱글톤이다.
    * 싱글톤 패턴
    하나의 클래스가 하나의 객체만을 생성하도록 하는 디자인 패턴이다
    
    * 생성자를 private으로 설정해서 클래스 외부에서 객체 생성 불가능 하도록함 
    * 클래스 내부의 static 메소드로 객체 생성 -> 메소드는 하나인데
    메소드 실행시마다 새로운 객체가 생성되는 문제가 생김  
  ```private static Singleton singleton; 
    if(singleton == null){ //객체 생성 }
    ```  

    요약 : 클래스 밖에서 생성 못하게 막고 메소드로만 생성하게 하되
    단 하나의 객체만 생성하도록 static 이용
* throws 
    * 예외를 뒤로 미룰 수 있다. 메소드 내에서 catch 를 처리하는 것이 아니다.