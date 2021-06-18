# 자바 enum
* enum 키워드는 열거 형 (변경할 수없음) 을 선언하는 키워드임
* 열거 형은 상수 그룹을 나타내는 특수한 클래스이다
*  enum을 만들려면 클래스 또는 인터페이스 대신 enum 키워드를 사용하고, 상수를 쉼표로 구분한다  

```
class Fruit{
    public static final Fruit APPLE = new Fruit();
    public static final Fruit PEACH = new Fruit();
    public static final Fruit BANANA = new Fruit();
}
```  

를 enum 키워드를 사용하여 다음과 같이도 만들 수 있음  
```
enum Fruit{
    APPLE, PEACH,BANANA;
}
```  

여기에 생성자, 멤버변수, 멤버함수를 추가 할 수 있다.  
```
enum Fruit{
    APPLE("red"), PEACH("pink"),BANANA("yellow");
    private String color;
    public String getColor(){
        return this.color;
    }
    Fruit(String color){
        this.color = color;
    }
}
```  
* enum도 일종의 클래스이다. 
* 열거형 상수를 간편하게 사용하기 위한 필요에 의해 만든 문법이다. 기존의 문법 체계로는 이해가 안되는 부분이 있을 수 있다.