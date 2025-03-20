# JAVA 메서드

### I/O
```java
import java.io.*;
import java.util.*;
import java.lang.*;
//psvm 옆에 throws IOException 추가
BufferedReader br= new BufferedReader(new InputStreamReader(System.in));
StringTokenizer st;
st=new StringTokenizer(br.readLine());
n=Integer.parseInt(st.nextToken());

```

### StringBuilder
append(string s) : 문자열을 끝에 추가  
indexOf(string s) : 문자열의 처음 위치 반환  
reverse() : 문자열을 뒤집음  
size() : 길이 반환  
insert(int offset,string s) : 지정된 위치에 문자열 삽입  

### List
add(E e) : 리스트 끝에 요소 추가  
get(int index) : 해당 인덱스의 요소 반환  
remove(int index) : 특정 인덱스의 요소 삭제  

### Queue
```java
Queue<Integer>q=new LinkedList<>();
```
offer() : 큐의 끝에 요소 추가  
poll() : 맨 앞 요소 제거하고 반환  
peek() : 맨 앞 요소를 반환 (제거 X)  

### AbstractMap.SimpleEntry<K,V>
```java
AbstractMap.SimpleEntry<Integer,Integer>mp=new AbstractMap.SimpleEntry<>(1,2);
```
getKey() : 키 반환  
getValue() : 값 반환  

### Stack
push(E e) : 스택의 맨 위에 요소 추가  
pop() : 맨 위 요소 제거 및 반환  
peek() : 맨 위 요소를 확인  

### Deque
```java
Deque<Integer>dq=new ArrayDeque<>();
```
addFirst(E e) : 덱 앞에 요소 추가  
addLast(E e) : 덱 뒤에 요소 추가  
pollFirst() : 맨 앞 요소 제거하고 반환  
pollLast() : 맨 뒤 요소 제거하고 반환    
