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
