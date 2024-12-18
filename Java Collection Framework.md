# Java Collection Framework

Java 컬렉션 프레임워크는 데이터를 관리하는 여러 자료 구조와 이를 처리하는 알고리즘을 제공하는 자바 클래스들의 모음입니다. 자바는 C 언어처럼 개발자가 직접 자료 구조를 구현할 필요 없이, 이미 최적화된 컬렉션 클래스를 제공하여, 쉽게 사용할 수 있습니다. 주요 컬렉션은 `Collection`과 `Map` 인터페이스로 나뉘며, 이들은 다양한 자료 구조를 효율적으로 처리합니다.

### 1. **컬렉션 프레임워크의 장점**

- **객체지향적 설계**: 컬렉션은 객체지향적 설계로 표준화되어 있어 사용법을 익히기 쉽고, 재사용성이 높습니다.
- **고성능**: 데이터 구조 및 알고리즘이 JVM에 최적화되어 있어 성능이 뛰어납니다.
- **API 간 호환성**: 다양한 컬렉션들이 상위 인터페이스를 공유하여, 서로 호환성이 좋습니다.
- **소프트웨어 재사용**: 이미 구현된 컬렉션을 재활용하여 새로운 알고리즘을 만들 수 있습니다.

### 2. **컬렉션 프레임워크의 구조**

컬렉션 프레임워크는 크게 두 가지 주요 인터페이스로 나뉩니다.

- **`Collection` 인터페이스**: `List`, `Set`, `Queue` 등이 이 인터페이스를 구현하여, 데이터를 저장하고 조작하는 다양한 방법을 제공합니다.
- **`Map` 인터페이스**: 키-값 쌍으로 데이터를 저장하며, 주로 `HashMap`, `TreeMap` 등의 클래스로 구현됩니다.

### 3. **주요 컬렉션 클래스**

### **Collection 인터페이스**

- **List**: 순서가 유지되며 중복을 허용하는 자료 구조입니다. `ArrayList`, `LinkedList` 등이 대표적입니다.
- **Set**: 순서가 없고, 중복을 허용하지 않는 자료 구조입니다. `HashSet`, `TreeSet` 등이 있습니다.
- **Queue**: 선입선출(FIFO) 방식의 자료 구조입니다. `PriorityQueue`, `LinkedList` 등이 이를 구현합니다.

### **Map 인터페이스**

- **Map**: 키-값 쌍으로 데이터를 저장하며, 중복된 키를 허용하지 않습니다. `HashMap`, `TreeMap` 등이 있습니다.

### 4. **Iterable 인터페이스**

컬렉션의 가장 상위 인터페이스로, `Iterator`를 통해 데이터를 순회할 수 있도록 합니다. `Collection`과 `Map`에서 데이터를 순회할 때 `Iterator`를 사용합니다.

### 5. **특징**

- **Primitive 타입 저장 불가**: 자바의 기본 자료형(예: `int`, `double`)은 컬렉션에 저장할 수 없으며, **박싱(Boxing)**을 통해 객체로 변환해야 합니다. 예를 들어, `int`는 `Integer` 객체로 변환하여 저장합니다.
- **다형성**: 컬렉션은 다형성을 활용하여 다양한 종류의 컬렉션 자료형을 동일한 타입으로 처리할 수 있습니다.

### 6. **주요 클래스 설명**

- **`ArrayList`**: 배열 기반의 리스트로, 데이터의 저장 순서를 유지하며 중복을 허용합니다. 데이터를 추가하고 삭제하는 데 적합하지만, 중간에 삽입/삭제 시 성능이 떨어질 수 있습니다.
- **`LinkedList`**: 노드 기반의 리스트로, 삽입과 삭제가 빠르지만, 임의 접근은 느립니다. `Queue`, `Deque`로도 사용 가능합니다.
- **`HashSet`**: 중복을 허용하지 않는 집합으로, 빠른 검색 성능을 자랑합니다. 순서는 보장되지 않습니다.
- **`TreeSet`**: 중복을 허용하지 않으며, 요소를 정렬된 순서로 저장합니다.
- **`HashMap`**: 키-값 쌍으로 데이터를 저장하는 맵으로, 검색이 빠르고, 순서는 보장되지 않습니다.
- **`LinkedHashMap`**: `HashMap`과 비슷하지만, 삽입된 순서대로 데이터를 저장합니다.

### 7. **기타**

- **`PriorityQueue`**: 우선순위가 높은 요소부터 꺼내는 큐로, `Comparable`을 구현한 객체들을 사용하여 우선순위를 관리합니다.
- **`Deque`**: 양쪽 끝에서 데이터를 삽입하고 삭제할 수 있는 큐입니다. `ArrayDeque`, `LinkedList`로 구현됩니다.