# 목차

## 1. Reflection 개요
___.class, Class.forName(packageName.className), ___.getClass()

## 2. 객체 생성과 생성자
### 2-1. 생성자 탐색 및 객체 생성.
Constructor&lt;T&gt;, getDeclaredConstructors(), getConstructors()
### 2-2. 생성자의 접근제어자별로 다른 사용법
setAccessible(true)
### 2-3. 클래스의 접근제어자별로 다른 사용법
package-private으로 정의된 class들 간의 의존성 주입 실습

## 3. 필드
### 3-1. 필드 객체를 활용한 Object - Json 변환기 예제 (Primitive, Reference, Array)
clazz.getDeclaredFields(), field.getType(), field.get(instance), clazz.getComponentType()

## 4. 배열
### 4-1. 배열 생성 및 초기화
- 생성: Array.newInstance(Class, Length)
- 조회: Array.get(Object, i)
- 수정: Array.set(Object, i, Value)
- 길이: Array.getLength(Object)

## 5. 메서드
## 5-1. 메서드 기본 API
- 메서드명: .getName()
- 파라미터타입: .getReturnType().getTypeName()
- 리턴타입: .getReturnType()
## 5-2. 부모 클래스가 존재하는 경우
- 본인클래스의 메서드만 조회(접근제어자 상관X): getDeclaredMethods()
- 부모클래스의 메서드 포함 조회(public만): getMethods()
## 5-3. 리플렉션을 이용한 다형성 구현 예제
- 메서드실행: method.invoke(Instance, args)

## 6. 제어자
- 접근제어자: public, private, protected, package-private
- 기타제어자: interface, abstract, synchronized, transient, static, final, native, etc..
- 제어자취득: clazz.getModifiers(), method.getModifiers(), field.getModifiers()
- 제어자판단: Modifier.isInterface(modifier), Modifier.isStatic(), etc...

## 7. 어노테이션
### 7-1. 어노테이션 탐색
- @Interface, @Retention(RetentionPolicy.~~~), @Target(ElementType.~~~)
### 7-2. 어노테이션을 활용한 Connection 초기화 예제
- clazz.getAnnotation(Class.class)
### 7-3. 어노테이션 탐색
- clazz.isAnnotationPresent(어노테이션명.class)
### 7-4. 어노테이션을 활용한 그래프탐색 예제
### 7-5. 필드 어노테이션
### 7-6. 반복 가능한 어노테이션 (RepeatableAnnotation)

## 8. 동적 프록시
### 8-1. 보안, 캐싱, 지연초기화, RPC 등에 활용
### 8-2. 동적 프록시를 활용한 실행 가로채기 (InvokationHandler)
