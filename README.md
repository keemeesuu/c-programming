# c-programming
C programming

---

<!-- # Type, 데이터 출력 -->

# 🎯 C언어의 특징

# 🎯 제어문자

`\n` : new line. 다음줄 이동.  
`\b` : backspace. 한 칸 왼쪽으로 이동.  
`\t` : tab. 수평 탭이동(일정공간 띄움).  
`\r` : carriage return. 맨 앞으로 이동.  
`\a` : 소리발생.


# 🎯 Type

C언어 에서는 정수, 실수, 문자, 문자열이 있다.

`printf` 함수는 기본적으로 문자열을 출력하는 함수이며 숫자를 출력할 때는 변환 문자를 사용해야함.

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

## 📌 상수(constant)

값이 정해져 있고 변하면 안되는 경우 주로 사용.

## 📍 정수

0~9, +,- 기호를 사용하며 이를 10진수, 8진수, 16진수로 표현할 수 있다.

#### 진법, 진수

10진법 : 0~9까지 10개 숫자.  
10진수 : 0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15 

8진법 : 0~7까지 8개 숫자.  
8진수 : 0,1,2,3,4,5,6,7,10,11,12,13,14,15,16,17  

16진법 : 0~9까지 숫자, A~F까지 6개 영문자.  
16진수0,1,2,3,4,5,6,7,8,9,A,B,C,D,E,F)  

#### C언어에서의 진법 표현

8진수는 숫자 앞에 0, 16진수는 0x를 붙여 구분함.

`%o` : 8진수 출력  
`%x` : 10진수 출력  
`%X` : 16진수 출력  

```c
printf("%d\n", 12); // 12
printf("%d\n", 014); // 12
printf("%d\n", 0xc); // 12

printf("%o\n", 12); // 14
printf("%x\n", 12); // c
printf("%X\n", 12); // C
```

## 📍 실수

실수는 소수점 형태와 지수 형태로 표현 할 수 있다.  
지수형태 c언어 표기법  
0.0000314 -> 3.14e-5  
이와 같이 소수점 앞에 0이 아닌 유효 숫자 한 자리를 사용하여 지수 형태로 바꾼 것을 **정규화(normaliztion) 표기법** 이라 한다.

```c
// f : 지수형태의 실수를 소수점 형태로 출력
printf("%f\n", 1e6); // 1000000.000000
printf("%f\n", 1e-6); // 0.000001
printf("%.1f\n", 1e6); // 1000000.0
printf("%.2f\n", 1e6); // 1000000.00

// lf : 소수점 이하 표시
printf("%.7lf\n", 3.14e-5); // 0.0000314
printf("%.7lf\n", 31.4e-5); // 0.0003140

// le : 소수점 형태의 실수를 지수 형태로 출력 (정규화 표기법)
printf("%le\n", 0.0000314); // 3.140000e-5
printf("%.2le\n", 0.0000314); // 3.14e-5
```

## 📍 문자, 문자열 

문자 상수 : 작은따옴표(''). 변환문자 : %c  
문자열 상수 : 큰 따옴표(""). 변환문자 : %s  

문자나 문자열이나 보통 %s를 사용함


## 📍 비트와 바이트

컴퓨터는 모든 데이터를 bit(비트)로 변환함.
1bit는 0과 1.
bit가 8개면 1byte.