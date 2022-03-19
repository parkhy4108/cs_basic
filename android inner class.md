### inner class 에 관하여
> Kotlin 에서는 inner class 가 자바랑 다르단다. 뭐가 다른지 한번 알아보자.

뭐가 다르다는걸까??  
예를 들어 설명해보자. 
- 자바 : A 클래스 안에 B z클래스 정의
         B클래스는 자동으로 A 클래스의 내부 클래스
         B클래스 -> A클래스 안의 객체 참조 가능 
         
```kotlin
fun main(){
  val ex1 = Outer().Inner().foo()
  println(ex1)
  val ex2 = Outer.Nested().foo()
  println(ex2)
}

class Outer {
  private val bar : Int = 1
  inner class Inner {
   fun foo() = bar
  }

class Nested {
  private val bar : Int = 2
    fun foo() = bar
  }
}
```
