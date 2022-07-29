# 주요 클래스(Class) 정리   
## 1. Scanner
<br>

## 2. BufferedReader
<br>

## 3. Stringbuilder   
<br>

## 4-1. String   
* 문자열(String) : 2글자 이상, 큰따옴표("")로 표시   
   * 문자 : 1글자, 작은따옴표('')로 표시
   * 1글자라도 ""로 묶이면 문자열이 된다
<br>

## 4-2. StringTokenizer   
* 설명: 사용자가 지정한 __구분자__ 로 문자열을 나누어주는 클래스
* 토큰(Token) : 구분자로 쪼개어진 문자열
* java.util 패키지
   * ```import java.util.StringTokenizer;```   

__ex>__   
```
StringTokenizer st = new StringTokenizer(br.readLine(), " ");  // 공백으로 구분
```
<br>
