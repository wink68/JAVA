## 3.2. 연산자의 연산 방법


### (7) 삼항 연산자   
* 항이 3개인 연산자   
* 기본 구성: __```(참 또는 거짓) ? 참일때 연산결과 : 거짓일때 연산결과```__   

   * 참 또는 거짓 : 비교 연산자 or 논리 연산자가 들어올 수 있다

__ex1>__   
```
int test1 = (5 > 3) ? 5 : 3;
System.out.println(test1);

결과: 5  (참이므로, 참인 결과 5 출력)
```

__ex2>__
```
int test2 = 3;
System.out.println((test2 % 2 == 0) ? "짝수" : "홀수");

결과: 짝수
```

__ex2-2>__: 삼항 연산자 → if-else 구문으로 변환   
```
if (test2 % 2 == 0) {
    System.out.println("짝수");
} else {
    System.out.println("홀수");
}
```
