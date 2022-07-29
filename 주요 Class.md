# 주요 클래스(Class) 정리   
## 1. Scanner
<br>

## 2. BufferedReader
<br>

## 3-1. String   
### 1) 문자열
* 2글자 이상, 큰따옴표("")로 표시   
   * 문자 : 1글자, 작은따옴표('')로 표시
   * 1글자라도 ""로 묶이면 문자열이 된다   
<br>

* 플러스(+)로 문자끼리 합할 수 있음   
__ex>__   
```System.out.println("생활"+"코딩");```
<br>

* 큰따옴표를 문자열로 사용하고 싶을 때, 큰따옴표 앞에 __역슬래쉬(\)__ 활용   
__ex>__   
```System.out.println("egoing said \"Welcome programming world\"");```   
<br>

### 2) String 클래스   
* 문자열을 다루기 위한 클래스
* String 클래스 = 데이터(char[]) + 메소드(문자열 관련)   
* 내용을 변경할 수 없는 불변(immutable) 클래스   
   * 두 문자열을 합쳐서 새로운 객체를 생성 → 성능상 좋지 않음
<br>
<br>

## 3-2. StringBuilder   
* 가변(mutable) 객체   
   * 새로운 객체를 생성하는 것이 아니라, 기존의 데이터를 더하는 방식
<br>

#### ① ```str.append```   
* 값을 이어 붙이는 메소드   
__ex>__   
```
StringBuilder str1 = new StringBuilder("abcd");
str1.append("63");

결과: abcd63
```
<br>

#### ② ```str.insert(index, value)```   
* 특정 인덱스(원하는 위치)에 값을 삽입하는 메소드   
__ex>__   
```
StringBuilder str1 = new StringBuilder("abcdef");
str1.insert(2, "ttt");

결과: abtttcdef
```

#### ③ ```str.delete(index1, index2)```
* 특정 index1부터 index2까지 값을 삭제하는 메소드   
__ex>__
```
StringBuilder str1 = new StringBuilder("abtttcdef");
str1.delete(2, 5);

결과: abcdef
```

#### ④ ```str.replace(index1, index2, value)```   
* 원하는 부분을 다른 문자열로 대체
__ex>__   
```
StringBuilder str1 = new StringBuilder("abcd");
str1.replace(0, 2, "tistory.");

결과: tistory.cd
```

#### ⑤ ```str.reverse()```
* 문자열을 뒤집어 주는 메소드   
__ex>__   
```
StringBuilder str1 = new StringBuilder("abcd");
str1.reverse();

결과: dcba
```

#### ⑥
<br>
<br>

## 3-3. StringBuffer   
<br>


## 3-4. StringTokenizer   
* 설명: 사용자가 지정한 __구분자__ 로 문자열을 나누어주는 클래스
* 토큰(Token) : 구분자로 쪼개어진 문자열
* java.util 패키지
   * ```import java.util.StringTokenizer;```   

__ex>__   
```
StringTokenizer st = new StringTokenizer(br.readLine(), " ");  // 공백으로 구분
```
<br>
