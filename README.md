# c-programming
C programming

---

<!-- # Type, 데이터 출력 -->

# 🫧 C언어의 특징

# 🫧 제어문자

`\n` : new line. 다음줄 이동.  
`\b` : backspace. 한 칸 왼쪽으로 이동.  
`\t` : tab. 수평 탭이동(일정공간 띄움).  
`\r` : carriage return. 맨 앞으로 이동.  
`\a` : 소리발생.


# 🫧 Type

C언어 에서는 정수, 실수, 문자, 문자열이 있다.

`%d` : 정수
`%lf` : 실수

```c
printf("%d\n", 10);         // %d 위치에 10출력
printf("%lf\n", 3.4);       // $lf위치에 3.4를 소수점 이하 6자리까지 출력
printf("%.1lf\n", 3.4);     // 소수점 이하 첫재 짜리까지 출력(둘째 자리에서 반올림)
printf("%.1lf\n", 3.45);
printf("%.10lf\n", 3.45);   // 소수점 이하 10자리까지 출력

printf("%d + %d = %d\n", 10, 20, 10+20);
// 10 + 20 = 30
```

<br>

## ✨ 상수(constant)

값이 정해져 있고 변하면 안되는 경우 주로 사용.

### 정수 상수

0~9, +,- 기호를 사용하며 이를 10진수, 8진수, 16진수로 표현할 수 있다.

### 진법, 진수

10진법 : 0~9까지 10개 숫자.  
10진수 : 0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15
8진법 : 0~7까지 8개 숫자.  
8진수 : 0,1,2,3,4,5,6,7,10,11,12,13,14,15,16,17  
16진법 : 0~9까지 숫자 A~F까지 6개 영문자.  
16진수0,1,2,3,4,5,6,7,8,9,A,B,C,D,E,F)

### 진법 표현