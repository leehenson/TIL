# SQL과 테이블의 구조

</br>

## SQL

</br>

### SQL이란

**S** Structured   
**Q** Query   
**L** Language

SQL은 위의 약자이다. 관계형 데이터베이스는 표의 형태로 정리정돈이 되어있는데 이것을 **구조화**되었다고 한다. 구조화를 영어로 **Structured**라고 하는데 이것이 SQL의 첫번째 **S**이다.

**Query**는 사용자가 데이터베이스에게 데이터를 넣어줘, 읽어줘, 수정해줘, 삭제해줘, 스키마를 만들어줘, 등의 명령을 데이터베이스에게 **질의**(요청)하는데, 질의를 영어로 **Query**라고 한다. 이것이 SQL의 두번째 **Q**이다.

**Language**는 데이터베이스와 사용자 모두가 이해할 수 있는 즉, 공통의 약속에 따라서 데이터베이스 서버에게 사용자가 요청을 해야만 알아들을 수 있기 때문에 그 때 사용하는 언어가 **SQL**이라는 언어이다.

</br>

### SQL의 특징

1. 어떠한 컴퓨터 언어보다도 쉽다.   
컴퓨터 언어 중 가장 쉬운 언어 두 가지 => HTML, SQL

2. 중요하다.   
SQL이라는 컴퓨터 언어는 관계형 데이터베이스라는 카테고리에 속하는 제품들이 공통적으로 데이터베이스 서버를 제어할 때 사용하는 언어이다. 표준화까지 되어있다. 그렇기 때문에 압도적인 다수의 데이터베이스 시스템이 SQL을 통해 동작한다.

**가성비가 아주 뛰어난 컴퓨터 언어이다.**

</br>

## 표(Table)

</br>

### 표(Table)의 용어

</br>

<a href="https://ibb.co/pbcBG8J"><img src="https://i.ibb.co/djFw1qG/Table-1.jpg" alt="Table-1" border="0"></a>

</br>

표는 영어로 Table이다. 테이블은 x축과 y축으로 두 가지로 볼 수 있다.

x축 즉, 수평으로 되어 있는 것을 row 또는 record, 행이라고 한다. MySQL에서는 row라는 표현을 많이 쓴다.

y축 즉, 수직으로 되어 있는 것을 column, 열이라고 한다.

보통 데이터베이스에서 column은 데이터의 구조(타입)를 의미하고, row는 데이터 하나하나 즉, 데이터 자체를 의미한다.