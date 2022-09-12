# Static (정적 메서드)
- 인스턴스 없이 클래스에서 바로 호출 가능
   ``` JS
   class User {
    constructor(){}
    static create(){}
   }
   
   User.create(); // new User()로 선언하지 않고 바로 호출 가능
   ```
- staticMethod를 호출하면 this는 클래스 생성자가 된다.
- 정적 메서드 끼리는 this.스태틱함수명()으로 호출 가능하다.
- 인스턴스에서는 호출이 불가능하다.
- 특정 클래스의 인스턴스가 아닌 클래스 전체에 필요한 기능을 만들때 사용한다.
- 
