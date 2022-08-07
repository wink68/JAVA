# 주요 클래스(Class) 정리   
## 1. Scanner
<br>

## 2-1. BufferedReader
#### (1) ```InputStreamReader();```   
* 입력을 받는 클래스   
* ```import java.io.InputStreamReader```   
<br>

#### (2) BufferedReader의 객체 생성
```
- 나눠쓰기
InputStreamReader ir = new InputStreamReader(System.in);  // InputStreamReader의 객체 생성
BufferedReader br = new BufferedReader(ir);

- 한 줄로 쓰기
BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
```
<br>

#### (3) BufferedReader의 메소드   
#### ① read와 readLine
* __```read()```__   
   * 문자 하나를 읽어 int형으로 리턴   
* __```readLine()```__   
   * 입력값 데이터를 한 줄로 읽어서 String으로 바꾸는 메소드   
<br>

#### ② ```Integer.parseInt()```   
* 문자열을 숫자로 변환하는 메소드   
__ex>__   
```
int N3 = Integer.parseInt(br.readLine());   // readLine으로 받은 String데이터를 정수로 변환
```

#### ③ ```.close()```   
* BufferedReader 종료   
<br>
◇ 참고 자료   

: https://chloe-ki.tistory.com/entry/java-bufferedreader-and-bufferedwriter-methods-and-exception-handling   

: https://kjwan4435.tistory.com/98   

<br>
<hr>

## 2-2. BufferedWriter   
#### (1) ```OutputStreamReader();```   
* 출력하는 클래스   
* ```import java.io.OutputStreamReader```   
<br>

#### (2) BufferedWriter의 객체 생성   
```
BufferedWriter bw = new BufferedWriter(new OutputStreamReader(System.out));
```
<br>

#### (3) BufferedWriter의 메소드   
#### ① ```.write()```   
* 입력값 데이터를 출력하는 메소드   

#### ② ```.flush()```   
* 버퍼에 남아있는 데이터를 모두 출력해서 버퍼를 비워줌   

#### ③ ```.close()```   
* BufferedWriter 종료

<br>
<hr>

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

## 3-2. StringBuilder / StringBuffer 메소드   
* 가변(mutable) 객체   

   * 새로운 객체를 생성하는 것이 아니라, 기존의 데이터를 더하는 방식   
   
◇ 참고 자료: https://travelbeeee.tistory.com/444?category=845655
<br>
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

#### ⑥ ```str.substring(index1, index2)```
* 특정 부분 문자열을 잘라오는 것   

__ex>__
```
StringBuilder str1 = new StringBuilder("abcdef");
System.out.println(str1.substring(1, 3));

결과: bc
```

#### ⑦ ```str.indexOf("value")```   
* value의 위치를 확인하는 메소드 (큰따옴표)  

__ex>__   
```
StringBuilder str1 = new StringBuilder("abcdef");
System.out.println(str1.indexOf("a"));

결과: 0
```

#### ⑧ ```str.length()```
* 문자열 길이를 확인하는 메소드   

__ex>__   
```
StringBuilder str1 = new StringBuilder("abcdef");
System.out.println(str.length());

결과: 6
```

#### ⑨ ```str.setLength()```
* 문자열 길이 변경   

__ex>__   
```
StringBuilder str1 = new StringBuilder("abcdef");
str1.setLength(2);
System.out.println(str1);

결과: ab
```
<br>
<hr>

## 3-3. StringTokenizer   
* 설명: 사용자가 지정한 __구분자__ 로 문자열을 나누어주는 클래스
* 토큰(Token) : 구분자로 쪼개어진 문자열
* java.util 패키지
   * ```import java.util.StringTokenizer;```   

__ex>__   
```
StringTokenizer st = new StringTokenizer(br.readLine(), " ");  // 공백으로 구분
```

◇ 참고 자료   
: https://blog.naver.com/dldudcks1779/222252355968
<br>
<br>

#### ① ```.nextToken()```
* 데이터를 토큰(Token) 단위로 불러옴    

__ex>__
```
0 12 0 4 0 0의 데이터를
0, 12, 0, 4, 0, 0 각각 불러옴
```

#### ② ```countTokens()```   
* 토큰(Token)의 개수를 세려줌   

__ex>__   
```
String str1 = "abc def";
StringTokenizer str2 = new StringTokenizer(str1, " ");

System.out.println(str2.countTokens());

결과: 2
```

#### ③ ```hasMoreTokens()```
* 반환할 Token이 남아있는지 여부를 true/false형태로 반환   

__ex>__   
```

String str1 = "abc def";
StringTokenizer str2 = new StringTokenizer(str1, " ");

System.out.println(str2.hasMoreTokens());

결과: true
```
<br>
<hr>

## 3-4. charAt()   
* 특정 위치(index값)의 문자열을 불리오는 방법   
* 아스키 코드
   * 숫자 0은 아스키 코드값 48   
   * 문자열 '0' 또는 숫자 48을 빼줘야 원하는 정수값이 나옴   

__ex>__   
```
String str = "1 3";
int A = str.charAt(0);       // 결과: 정수값 49
int B = str.charAt(0) -'0';  // 결과: 정수값 1  / 문자열 '0'을 빼줌
int C = str.charAt(0) -48;   // 결과: 정수값 1  / 정수 48을 빼줌
```

◇ 참고 자료   
: https://cokes.tistory.com/m/80

<br>
<hr>

## 4-1. BigInteger
* 선언: __```BigInteger 변수명 = new BigInteger();```__   

   * 엄청 큰 수를 계산할 때
   
### 1) 계산   
* 덧셈 : ```변수명.add();```   
* 뺄셈 : ```변수명.substract();```   
* 곱셈 : ```변수명.multiply();```
* 나눗셈 : ```변수명.divide();```   
* 나머지 : ```변수명.remainder();```   
<br>

### 2) BigInteger 형 변환   
* int → BigInteger : ```BigInteger 변수1 = BigInteger.valueOf(정수값);```   

* BigInteger → int : ```int 변수2 = 변수1.intValue();```   
* BigInteger → long : ```long 변수2 = 변수1.longValue();```
* BigInteger → float : ```float 변수2 = 변수1.floatValue();```   
* BigInteger → double : ```double 변수2 = 변수1.doubleValue();```   
* BigInteger → String : ```String 변수2 = 변수1.toString();```   
<br>

### 3) BigInteger 두 수 비교   
```
BigInteger A = new BigInteger("정수값");
BigInteger B = new BigInteger("정수값");

int 변수명 = A.compareTo(B);  // 
System.out.println(변수명);   // A가 더 크면 1, 같으면 0,  B가 더 크면 -1
```

◇ 참고 자료   

: 백준 단계별 7-8번 문제   
: https://coding-factory.tistory.com/604   

<br>
<hr>

## 5. Math   
### 1) Math.pow()
* pow = power (제곱)   
   * 2의 4제곱 = 2 to the power 4 is 16

* 선언 : __```Math.pow(x, y)```__   
   * x의 y제곱 값 출력

__ex>__   
```
System.out.print(Math.pow(3, 2);         // 9.0
System.out.print((int) Math.pow(3, 2);   // 9
```
<br>

### 2) Math.sqrt()   
* 제곱하면 X가 되는 수 출력 = X의 제곱근 = 루트   

* 선언: __```Math.sqrt(z)```__   

__ex>__   
```
System.out.print(Math.sqrt(4));         // 2.0
System.out.print((int) Math.sqrt(4));   // 2
```
<br>

◇ 참고 자료   
: https://blog.naver.com/scyan2011/221656914043
