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
### Character
isLetter(Character ch) : 문자인지 아닌지 true,false 반환  
isUpperCase(Character ch) : 대문자인지 아닌지 ""  
isLowerCase(Character ch) : 소문자인지 아닌지 ""  

### String
charAt(int index) : 해당 인덱스의 문자를 반환  
substring(int start,int end) : 시작~끝-1 까지 문자열을 반환  
startsWith(String s) : 처음부터 s와 매칭하여 맞는지 boolean 반환  
endsWith(String s) : 마지막 부분 s와 매칭하여 맞는지 boolean 반환  
  
### StringBuilder
append(string s) : 문자열을 끝에 추가  
indexOf(string s) : 문자열의 처음 위치 반환 #없으면 -1 반환  
delete(int start,int end) : 범위 삭제  
deleteCharAt(int index) : 해당 원소 삭제  
reverse() : 문자열을 뒤집음  
size() : 길이 반환  
insert(int offset,string s) : 지정된 위치에 문자열 삽입  

### List
add(E e) : 리스트 끝에 요소 추가  
get(int index) : 해당 인덱스의 요소 반환  
remove(int index) : 특정 인덱스의 요소 삭제  
```java
//정렬 람다식
list.sort((t1,t2)->{
            int val=Long.compare(t2.count,t1.count);
            if(val!=0){
                return val;
            }
            return Long.compare(t1.order,t2.order);
});
```

### Map<K,V>
put(K key, V value) : 새로운 키-값 추가  
get(K key) : 키에 해당하는 값 반환  
getOrDefault(K key, V defaultValue) : 키가 없으면 기본값 반환  
containsKey(K key) : 값이 존재하는지 확인  
remove(K key) : 해당 키 삭제  
```java
for(Map.Entry<Integer,Integer>temp:mp.entrySet()){
  temp.getKey(),temp.getValue()
}
```

### AbstractMap.SimpleEntry<K,V>
```java
AbstractMap.SimpleEntry<Integer,Integer>mp=new AbstractMap.SimpleEntry<>(1,2);
```
getKey() : 키 반환  
getValue() : 값 반환  

### Queue
```java
Queue<Integer>q=new LinkedList<>();
```
offer() : 큐의 끝에 요소 추가  
poll() : 맨 앞 요소 제거하고 반환  
peek() : 맨 앞 요소를 반환 (제거 X)  

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

### PriorityQueue
```java
static PriorityQueue<AbstractMap.SimpleEntry<Integer,Integer>>pq=new PriorityQueue<>((t1,t2)->{
        return Integer.compare(t1.getValue(),t2.getValue());
    }); // 맨위에 오는 Element는 기본 정렬과 같음
```
offer(E e) : 큐에 요소를 추가  
peek() : 가장위에 있는 요소를 확인(반환x)  
poll() : 가장위의 있는 요소를 반환  
