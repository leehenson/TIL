Chapter 2. 변수

# 3. 진법

## 3.1 10진법과 2진법

변수에 값을 저장하면 10진수로 저장되는 것처럼 설명되지만,  컴퓨터는 2진수(0과 1) 밖에 모르기 때문에 2진수로 바뀌어 저장된다.

![image](https://ifh.cc/g/4S18YR.png)

이처럼 2진법은 0과 1로만 데이터를 표현하기 때문에 10진법에 비해 많은 자리수를 필요로 한다.

이것은 10진수에서 9보다 큰 수를 표현하기 위해서는 두 자리의 10진수가 필요한 것과 같다.

![image](https://ifh.cc/g/vKLq9m.png)

그래서 2진수 1에 1을 더하면 2가 아닌 10이 되고, 2진수 11에 1을 더하면 12가 아닌 100이 된다.

![image](https://ifh.cc/g/Hj9RND.png)

자리수가 많아지긴 해도 2진수는 10진수를 온전히 표현할 수 있다. 게다가 덧셈이나 뺄셈 같은 연산도 10진수와 동일하다.

</br>

## 3.2 비트(bit)와 바이트(byte)

한 자리 2진수를 '비트(bit, binary digit)'라고 하며, 1 비트는 컴퓨터가 값을 저장할 수 있는 최소단위이다. 그러나 1비트는 너무 작은 단위이기 때문에 1 비트 8개를 묶어서 '바이트(byte)'라는 단위로 정의해서 데이터의 기본 단위로 사용한다.

이 외에도 '워드(word)'라는 단위가 있는데, **'워드(word)'는 'CPU가 한 번에 처리할 수 있는 데이터의 크기'를 의미한다.** 워드의 크기는 CPU의 성능에 따라 달리진다. 예를 들어 32비트 CPU에서 1워드는 32비트(4 바이트)이고, 64 비트 CPU에서는 64 비트(8 바이트)이다.

![image](https://ifh.cc/g/fQm3Ww.png)

n비트로 2^n개의 값을 표현할 수 있다. 그리고 n비트로 10진수를 표현한다면, 표현가능한 10진수의 범위는 0 ~ 2^n - 1이 된다.

> **n비트로 표현 할수 있는 10진수**   
**값의 개수 : 2^n**   
**값의 범위 : 0 ~ 2^n - 1**

</br>

## 3.3 8진법과 16진법

2진법은 오직 0과 1, 두 개의 기호만으로 값을 표현하기 때문에 2진법으로 값을 표현하면 자리수가 상당히 길어진다는 단점이 있다. 이러한 단점을 보완하기 위해 2진법 대신 8진법이나 16진법을 사용한다.

**8진수는 2진수 3자리를, 16진수는 2진수 4자리를 각각 한자리로 표현할 수 있기 때문에 자리수가 짧아져서 알아보기 쉽고 서로 간의 변환방법 또한 매우 간단하다.**

![image](https://ifh.cc/g/HpKQhr.png)

8진법은 값을 표현하는데 8개의 기호가 필요하므로 0\~7의 숫자를 기호로 사용하면 되지만, 16진법은 16개의 기호가 필요하므로 0\~9의 숫자만으로는 부족하다. 그래서 6개의 문자(A~F)를 추가로 사용한다. 예를 들어 16진수 A는 10진수로 10이고, F는 16이다.

### 2진수를 8진수, 16진수로 변환

2진수를 8진수로 변환하려면, 2진수를 뒤에서부터 3자리씩 끊어서 그에 해당하는 8진수로 바꾸면 된다. 8은 2^3이기 때문에, 8진수 한 자리가 2진수 3자리를 대신할 수 있는 것이다. 2진수를 16진수로 변환하는 방법 역시 이와 비슷한데, 3자리가 아닌 3자리씩 끊어서 바꾼다는 점만 다르다.

</br>

## 3.4 정수의 진법 변환

### 10진수를 n진수로 변환

10진수를 다른 진수로 변환하려면, 해당 진수로 나누고 나머지 값을 옆에 적는 것을 더 이상 나눌 수 없을 때까지 반복한 다음 마지막 몫과 나머지를 아래부터 위로 순서대로 적으면 된다.

즉, n진수로 변환하려면, n으로 반복해서 나누기만 하면 된다.

### n진수를 10진수로 변환

어떤 진법의 수라도 10진수로 변환하는 방법은 똑같다. 각 자리의 수에 해당 단위의 값을 곱해서 모두 더하면 된다.

</br>

## 3.5 실수의 진법변환

### 10진 소수점수를 2진 소수점수로 변환하는 방법

10진 소수점수를 2진 소수점수로 변환하는 방법은 이와 반대로 소수점수에 2를 계속 곱한다.

1. **10진 소수에 2를 곱한다.**
2. **위의 결과에서 소수부만 가져다가 다시 2를 곱한다.**
3. **1.과 2.의 과정을 소수부가 0이 될 때까지 반복한다**

위의 결과에서 정수부만을 위에서 아래로 순서대로 적고, '0.'을 앞에 붙이면 된다.

### 2진 소수점수를 10진 소수점수로 변환하는 방법

정수부와 똑같이 각 자리의 수에 해당 단위의 값을 곱해서 모두 더하면 된다.

</br>

## 3.6 음수의 2진 표현 - 2의 보수법

n비트의 2진수로 표현할 수 있는 값의 개수는 모두 2^n이므로, 4비트의 2진수로는 모두 2^4(=16)개의 값을 표현할 수 있다. 이 값을 모두 '부호없는 정수(0과 양수)'의 표현에 사용하면 0~15까지 표현할 수 있다.

그러면 4비트의 2진수로 부호있는 정수, 즉 양수와 음수를 모두 표현하려면 4비트 2진수의 절반인 8개는 0으로 시작하고, 나머지 절반은 1로 시작하니까, 1로 시작하는 2진수를 음수표현에 사용하면 된다. '왼쪽의 첫 번째 비트(MSB)'가 0이면 양수, 1이면 음수이므로 첫 번째 비트만으로 값의 부호를 알 수 있게 된다.

![image](https://ifh.cc/g/SM3cYc.png)

음수를 이렇게 배치하면, 양수의 첫 번째 비트만 1로 바꾸면 음수가 된다는 장점이 있다. 그러나, 두 수를 더했을 때 2진수로 0이 도지 않는다는 것과 0이 두 개(0, -0) 존재한다는 단점이 있다. 게다가 2진수가 증가할 때 10진 음수는 감소한다.

![image](https://ifh.cc/g/wPHCPz.png)

그러나 위와 같이 '2의 보수법'에 의해 음수를 배치하면, 절대값이 같은 양수와 음수를 더했을 때 2진수로도 0을 결과로 얻으므로 부호를 신경쓰지 않고 덧셈할 수 있게 된다.

그리고 2진수가 증가할 때 10진수 음수가 감소한다는 모순도 없어졌다. 다만, 첫 번째 비트를 바꾸는 것만으로 값의 부호를 바꿀 수 없게 되었다.

### 2의 보수법

어떤 수의 'n의 보수'는 **더했을 때 n이 되는 수**를 말한다. 7의 '10의 보수'는 3이고, 3의 '10의 보수'는 7이다. 3과 7은 '10의 보수의 관계'에 있다고 한다. '2의 보수 관계' 역시, 더해서 2가 되는 두 수의 관계를 말하며 10진수 2는 2진수로 '10'이다. 2진수로 '10'은 **자리올림이 발생하고 0이 되는 수**를 뜻한다. 그래서 '2의 보수 관계'에 있는 두 2진수를 더하면 '(자리 올림이 발생하고) **0이 된다.**'

2진수 '0101'와 '1011'은 서로 '2의 보수 관계'에 있으며, 이 두 2진수를 더하면 0이 된다. 이 덧셈이 10진수로도 0이 되려면, 2진수 '0101'가 10진수로 5니까. 2진수 '1011'은 10진수로 -5이어야 한다.

![image](https://ifh.cc/g/Z9rx31.png)

이처럼 서로 '2의 보수 관계'에 있는 두 2진수로 5와 -5처럼 절대값이 같고 부호가 다른 두 10진수를 표현하는 것을 '2의 보수법'이라고 하며, 현재 대부분이 시스템이 '2의 보수법'으로 부호있는 정수를 표현한다.

### 음수를 2진수로 표현하기

10진 음의 정수를 2진수로 변환하려면, 먼저 10진 음의 정수의 절대값을 2진수로 변환한다. 그 다음에 이 2진수의 '2의 보수'를 구하면 된다.

### 2의 보수 구하기

> **2의 보수 = 1의 보수 + 1**

'1의 보수'는 **0을 1로, 1을 0으로**만 바꾸면 되므로 구하기 쉽다. 예를 들어, 2진수 '0101'의 '1의 보수'는 '1010'이다. 여기에 1을 더하기만 하면 '1011' 2의 보수가 된다. 

### 왜 '1의 보수 + 1'은 '2의 보수'인가?

어떤 2진수가 있을 때, 이 2진수의 1의 보수는 더하면 모든 자리가 1이 된다.

여기서 1을 더하게 되면 올림(carry)이 발생하지만 4비트를 넘는 값이라 저장할 공간이 없어서 버려지므로 '0000'된다.

어떤 수에 '1의 보수 + 1'을 더하면 0이 되므로 '1의 보수 + 1'은 '2의 보수'와 같다는 것이 증명된다.

> **음수의 2진 표현을 구하는 방법**
> 1. **음수의 절대값을 2진수로 변환한다.**   
\: -5의 절대값인 5를 2진수로 변환한다. 10진수 5를 2진수로 변환하면 '0101'이다.
> 2. **1.에서 구한 2진수의 1을 0으로 0은 1로 바꾼다(1의 보수 구하기)**   
\: '0101'이 '1010'이 된다.
> 3. **2. 의 결과에 1을 더한다.(2의 보수 구하기, 1의 보수 + 1)**   
\: '1010'에 1을 더하면 '1011'이 되고, 이것이 -5의 2진 표현이다.