# 인터넷과 데이터베이스

**MySQL은 내부적으로 인터넷을 활용할 수 있도록 고안된 시스템이다.**

</br>

## Internet

인터넷이 동작하기 위해서는 최소 2대의 컴퓨터가 필요하다.

**인터넷의 의미는 각자 흩어져있는 컴퓨터들이 인터넷으로 연결되면서 컴퓨터들간의 사회가 만들어진 것이다. 컴퓨터간의 사회가 만들어졌다는 것은 한 대의 컴퓨터가 갖고 있는 한계를 초월하게 되었다는 것이다.**

</br>

### 인터넷의 원리

두 대의 컴퓨터 중 한 대의 컴퓨터는 정보를 다른 컴퓨터에게 요청을 한다. 그리고 또 한 대의 컴퓨터는 요청한 정보를 응답한다. 웹을 예를 들 수 있는데 웹이 동작하기 위해서는 인터넷이 필요하고, 인터넷 위에서 동작하기 때문에 두 대의 컴퓨터가 필요하다. 한 대의 컴퓨터에는 웹브라우저가 설치되어있고, "google.com"과 같은 도메인 네임을 입력하면 그 도메인 네임 주소에 해당하는 컴퓨터를 찾아간다. 그러면 그 주소에 해당하는 컴퓨터가 요청한 정보를 요청한 컴퓨터에게 응답하고, 웹브라우저 표시된다.

인터넷 위에서 동작하는 컴퓨터들은 정보를 요청하는 쪽과 응답하는 쪽으로 나뉘게 된다. 요청하는 쪽을 "Client" 한국말로 고객, 갑이라고 하고, 응답하는 족은 서비스를 제공한다는 뜻으로 "Server" 한국어로는 사업자, 서비스 제공자, 을이라고 한다. **즉, 인터넷이라는 것은 갑과 을에 해당하는 컴퓨터가 서로 정보를 요청하고 응답하면서 동작하는 시스템이다.**

그리고 Client 컴퓨터는 Server 컴퓨터에게 정보를 요청하는데 이 관계가 웹이라면, 정보를 요청하는 컴퓨터에 설치된 프로그램은 웹브라우저이다. 다른 말로 웹 클라이언트라고 할 수 있다. 그리고 응답하는 서버 컴퓨터에 설치되어있는 웹을 위한 프로그램을 웹 서버라고 한다. 또 이 관계가 게임이라면 사용자의 컴퓨터에 설치되어 있는 프로그램을 게임 클라이언트라고 하고, 게임 회사의 서버에 설치되어 있는 프로그램을 게임 서버라고 한다.

**Client와 Server는 인터넷을 이해하는 핵심적인 열쇠라고 할 수 있다.**

</br>

## MySQL

MySQL을 설치하면 두 개의 프로그램을 동시에 설치한다. 하나는 데이터베이스 클라이언트고 또 하나는 데이터베이스 서버이다. 그리고 데이터베이스 서버에는 실제로 데이터가 저장이 되고, 그리고 데이터베이스 클라이언트를 통해서 데이터베이스 서버에 접속할 수 있다. 데이터베이스 서버는 직접 다룰 수 없고, 데이터베이스 서버는 반드시 어떠한 형태로든 데이터베이스 클라이언트를 사용해야 한다.

</br>

### 데이터베이스 클라이언트

mysql에서는 커맨드라인에 `mysql`이라고 입력했을 때 실행되는 명령어 기반의 프로그램이 데이터베이스 클라이언트이다. `MySQL Monitor`가 데이터베이스 클라이언트 중에 하나이고, MySQL을 설치하면 MySQL 서버에 접속할 수 있도록 기본적으로 제공하는 기본 클라이언트이다. 그리고 `MySQL Monitor`는 명령어를 통해서 데이터베이스 서버를 제어하는 프로그램이다.

그리고 "MySQL Workbench"라는 MySQL 클라이언트 프로그램이 있는데, 이 프로그램을 사용하면 GUI 환경에서 마치 엑셀을 다룰 듯이 데이터베이스를 다룰 수 있다.

</br>

### 데이터베이스 클라이언트와 데이터베이스 서버

데이터베이스 클라이언트와 데이터베이스 서버를 사용하므로써 데이터베이스 서버에 데이터를 저장하고, 전세계에 있는 수많은 데이터베이스 클라이언트들이 데이터베이스 서버를 중심으로 데이터를 넣고, 빼고 하는 폭발적인 효과를 얻게 된다.