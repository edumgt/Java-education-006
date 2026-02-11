# Java 교육용 예제 저장소

이 저장소는 **자바(Java) 핵심 문법과 객체지향/고급 기능을 단계적으로 학습**하기 위한 예제 모음입니다.
각 폴더는 하나의 주제(예: 추상 클래스, 인터페이스, 예외 처리, 컬렉션, 제네릭, 스레드 등)를 다루며, `CE01Example_XX.java` 파일을 중심으로 실행 흐름을 확인할 수 있도록 구성되어 있습니다.

---

## 1) 기술 스택

### 언어
- **Java**
  - 기본 문법부터 OOP, 컬렉션, 람다, 리플렉션, 파일/DB/스레드 등 핵심 주제를 폭넓게 다룹니다.

### 빌드/실행 방식
- 현재 저장소는 Maven/Gradle 프로젝트 구조가 아닌, **폴더별 단일 자바 소스 예제 구조**입니다.
- IDE(IntelliJ, Eclipse) 또는 `javac` / `java` 명령어로 개별 파일을 컴파일/실행하여 학습하기 좋습니다.

### 데이터 접근
- `db/` 예제를 통해 **데이터베이스 연동 기초**를 확인할 수 있습니다.

### 동시성
- `thread/` 예제를 통해 **스레드와 동기화 기초 개념**을 학습할 수 있습니다.

---

## 2) 소스 구조 안내

아래는 디렉터리별 학습 주제와 주요 파일입니다.

### `data_type/`
- 자바의 기본 데이터 타입/문법 입문 예제
- `CE01Example_02.java`

### `abstract/`
- 추상 클래스와 상속 구조 학습
- `CBase.java`, `CDerived.java`, `CE01Example_03.java`

### `interface/`
- 인터페이스 설계 및 구현체 분리
- `IWriter.java`, `IReleasable.java`, `CWriter_Console.java`, `CWriter_File.java`, `CE01Example_04.java`

### `exception/`
- 예외 클래스 정의 및 예외 처리 흐름
- `CException.java`, `CE01Example_05.java`

### `object/`
- 클래스/객체 개념과 멤버 활용
- `CCharacter.java`, `CE01Example_06.java`

### `wrapper/`
- Wrapper 클래스와 형 변환/유틸리티 활용
- `CE01Example_07.java`

### `Reflection/`
- Reflection 기초 사용법
- `CE01Example_08.java`

### `nested_class1/`, `nested_class2/`
- 내부 클래스/중첩 클래스와 관련 인터페이스 활용
- `nested_class1/COuter.java`, `nested_class1/CE01Example_09.java`
- `nested_class2/COuter.java`, `nested_class2/INested.java`, `nested_class2/CE01Example_10.java`

### `lambda/`
- 람다식, 함수형 인터페이스 기초
- `ICompare.java`, `CE01Example_11.java`

### `generic/`, `generic2/`
- 제네릭 타입과 컬렉션 구조 구현/활용
- `generic/CList_Linked.java`, `generic/CE01Example_13.java`, `generic2/CE01Example_12.java`

### `queue/`
- 큐 자료구조 개념 활용 예제
- `CE01Example_14.java`

### `collection/`
- 자바 컬렉션 프레임워크 사용
- `CE01Example_15.java`

### `thread/`
- 멀티스레드 기초 및 카운터 동작 예제
- `CCounter.java`, `CE01Example_17.java`

### `file/`
- 파일 입출력(IO) 처리
- `CE01Example_18.java`

### `db/`
- 데이터베이스 접근 기초
- `CE01Example_19.java`

---

## 3) 학습 추천 순서

아래 순서대로 진행하면 난이도를 점진적으로 높일 수 있습니다.

1. `data_type` → `object`
2. `abstract` → `interface`
3. `exception` → `wrapper`
4. `nested_class1` → `nested_class2`
5. `lambda` → `generic` → `generic2`
6. `queue` → `collection`
7. `file` → `db` → `thread` → `Reflection`

---

## 4) 실행 방법 (로컬 CLI 기준)

예시: `object/CE01Example_06.java` 실행

```bash
# 1) 컴파일
javac object/CCharacter.java object/CE01Example_06.java

# 2) 실행
java object.CE01Example_06
```

> 참고: 파일에 package 선언이 있는 경우, 디렉터리 구조와 실행 경로를 package 기준으로 맞춰서 컴파일/실행해야 합니다.

---

## 5) 이 저장소를 활용하는 방법

- 각 예제 파일을 읽고, 실행 결과를 먼저 예측한 뒤 실제 실행해보세요.
- 예외 처리/인터페이스/제네릭처럼 중요한 주제는 예제를 직접 수정해보며 동작 차이를 확인하면 학습 효과가 큽니다.
- 스레드, DB, 파일 IO는 실무와 연결되는 주제이므로 작은 미니 실습(로그 저장기, 간단 DAO 등)으로 확장해보는 것을 추천합니다.

---

## 6) 대상 독자

- Java 입문자 ~ 중급 초반
- 객체지향 설계의 핵심 요소(추상화/다형성/인터페이스)를 실습 중심으로 익히고 싶은 학습자
- 컬렉션, 람다, 제네릭, 파일/DB/스레드까지 폭넓게 훑고 싶은 교육 과정 수강생
