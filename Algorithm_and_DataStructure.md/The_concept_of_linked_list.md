# Linked List의 개념

</br>

## Linked List란

Linked List는 컴퓨터의 자료를 저장하는 구조의 한 종류이다. 일렬로 연결된 데이터를 저장할 때 사용한다.

데이터를 저장할 공간이 있으면, 그 안에 다음 데이터의 주소를 가지고 있는 구조이다.

</br>

## 배열과의 차이

배열(Array)은 배열방들이 물리적으로 한 곳에 모여있다. 그 때문에 배열방 크기를 한번 정하면 늘리거나 줄일 수가 없다. 그에 반해서 Linked List는 데이터를 중간에 삽입을 하고 싶으면 앞에 노드가 가지고 있던 주소를 자기가 갖고 앞에 노드의 주소에 자기의 주소를 넣어주면 된다. 반대로 링크를 빼고 싶을 때에는 해당 노드가 갖고있던 다음 노드의 주소를 앞에 노드에게 주면 된다.

하지만 삭제된 노드는 메모리를 잡아먹고 있는데 Java 같은 프로그래밍 언어에서는 이렇게 안 쓰이는 데이터들을 알아서 처리해주는데 C++ 같은 프로그래밍 언어에서는 반드시 안 쓰겠다고 명시를 해주어야 한다. 그래야 잡아먹고 있는 메모리를 다른 곳에서 쓸 수가 있다.

</br>

## Linked List의 특징

Linked List는 노드들의 주소를 따라 일일이 찾아다녀야 하기 때문에 물리적으로 모여있는 배열보다 읽기 속도가 느릴 수가 있다. 그런데 삽입 및 삭제와 같은 수정을 할 때에는 배열 같은 경우, 배열방을 다시 만들고 복사하거나, 배열방에 데이터들을 하나하나 옮겨야 하기 때문에 느리다. 하지만 데이터의 길이가 정해져 있지 않은 데이터를 핸들링하거나 데이터 삽입 및 삭제와 같은 수정을 할 때에 Linked List는 다음 노드의 주소만 변경해주면 되기 때문에 더 사용하기 좋다.