Chapter 3. 연산자

# 2. 단항 연산자

</br>

## 2.1 증감 연산자 ++ --

증감연산자는 피연산자에 저장된 값을 1 증가 또는 감소시킨다. 증감연산자의 피연산자로 정수와 실수가 모두 가능하지만, 상수는 값을 변경할 수 없으므로 가능하지 않다.

대부분의 연산자는 피연산자의 값을 읽어서 연산에 사용할 뿐, 피연산자의 타입이나 값을 변경시키지 않는다. 오직 대입연산자와 증감연산자만 피연산자의 값을 변경한다.

> 증감연산자는 일반 산술 변환에 의한 자동 형변환이 발생하지 않으며, 연산결과의 타입은 피연산자의 타입과 같다.

> **증가 연산자(++)** 피연산자의 값을 1 증가시킨다.   
**감소 연산자(--)** 피연산자의 값을 1 감소시킨다.

일반적으로 단항 연산자는 피연산자의 왼쪽에 위치하지만, 증가 연산자 `++`와 감소 연산자 `--`는 양쪽 모두 가능하다. 피연산자의 왼쪽에 위치하면 '전위형(prefix)', 오른쪽에 위치하면 '후위형(postfix)'이라고 한다.

전위형과 후위형 모두 피연산자의 값을 1 증가 또는 감소시키지만, 증감연산자가 수식이나 메소드 호추렝 포함된 경우 전위형일 때와 후위형일 때의 결과가 다르다.

![image](https://ifh.cc/g/BSWT3V.png)

그러나 `++i;`와 `i++;`처럼 증감연산자가 수식이나 메소드 호출에 포함되지 않고 독립적인 하나의 문장으로 쓰인 경우에는 전위형과 후위형의 차이가 없다.

``` java
++i;    // i의 값을 1 증가시킨다.
i++;    // 이의 문장과 차이가 없다
```

예제 3-1 / ch3 / OperatorEx1.java
``` java
public class OperatorEx1 {

	public static void main(String[] args) {
		int i = 5;
		i++;	// i = i + 1;과 같은 의미이다. ++i;로 바꿔 써도 결과는 같다.
		System.out.println(i);
		
		i= 5;	// 결과를 비교하기 위해 i값을 다시 5로 변경.
		++i;
		System.out.println(i); 	
	}

}
```

```
6
6
```

예제 3-2 / ch3 / OperatorEx2.java
``` java
public class OperatorEx2 {

	public static void main(String[] args) {
		int i = 5, j = 0;
		
		j = i++;
		System.out.println("j = i++; 실행 후, i = " + i + ", j = " + j);
		
		i = 5;	// 결과를 비교하기 위해, i와 j의 값을 다시 5와 0으로 변경
		j = 0;
		
		j = ++i;
		System.out.println("j = ++i; 실행 후, i = " + i + ", j = " + j);
	}

}
```

```
j = i++; 실행 후, i = 6, j = 5
j = ++i; 실행 후, i = 6, j = 6
```

전위형은 변수(피연산자)의 값을 먼저 증가시킨 후에 변수의 값을 읽어오는 반면, 후위형은 변수의 값을 먼저 읽어온 후에 값을 증가시킨다.

증감연산자가 포함된 식을 이해하기 어려울 때는 다음과 같이 증감 연산자를 따로 떼어내면 이해하기가 쉬워진다. 전위형의 경우 증감연산자를 식의 이전으로,

![image](https://ifh.cc/g/1SZCaF.png)

후위형의 경우 증감연산자를 식의 이후로 뗴어내면 된다.

![image](https://ifh.cc/g/QfPXqv.png)

예제 3-3 / ch3 / OperatorEx3.java
``` java
public class OperatorEx3 {

	public static void main(String[] args) {
		int i = 5, j = 5;
		System.out.println(i++);
		System.out.println(++j);
		System.out.println("i = " + i + ", j = " + j);
	}

}
```

```
5
6
i = 6, j = 6
```

`i`는 값이 증가되기 전에 참조되므로, `println()`에게 `i`에 저장된 값 `5`를 넘겨주고 나서 `i`의 값이 증가하기 때문에 `5`가 출력되고, `j`의 경우 `j`에 저장된 값을 증가 시킨 후에 `println()`에게 값을 넘겨주므로 `6`이 출력된다. 결과적으로 `i`, `j` 모두 1씩 증가되어 `6`이 된다.

하나의 식에서 증감연산자의 사용을 최소화하고, **식에 두 번 이상 포함된 변수에 증감연산자를 사용하는 것은 피해야 한다.**

감소 연산자(--)는 피연산자의 값을 1 감소시킨다는 것만 빼면 증가 연산자와 동일하다.

</br>

## 2.2 부호 연산자 + -

부호 연산자 `-`는 피연산자의 부호를 반대로 변경한 결과를 반환한다. 피연산자가 음수면 양수, 양수면 음수가 연산의 결과가 된다.

부호 연산자는 `boolean`형과 `char`형을 제외한 기본형에만 사용할 수 있다.

> 부호 연산자는 덧셈, 뺄셈연산자와 같은 기호를 쓰지만 다른 연산자이다. 기호는 같아도 피연산자의 개수가 달라서 구별이 가능하다.

예제 3-4 / ch3 / OperatorEx4.java
``` java
public class OperatorEx4 {

	public static void main(String[] args) {
		int i = -10;
		i = +i;
		System.out.println(i);
		
		i = -10;
		i = -i;
		System.out.println(i);
	}

}
```

```
-10
10
```