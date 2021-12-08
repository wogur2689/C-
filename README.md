# C
C언어 공부 + 프로젝트

# 프로젝트 목록
 -C언어 계산기
 -코딩은행

# <1장> C언어란?

C언어의 탄생
-1972년 데니스 리치(Dennis Ritchie)가 유닉스(Unix)를 개발하기 위해 개발한 프로그래밍 언어

C언어의 특징
1. 절차지향 언어
   ▷ 시간의 흐름에 따라 정해진 절차를 실행
2. 간결하고 효율적인 언어
   ▷ 재귀 호출이 가능
   ▷ 포인터와 메모리 관리 기능으로 세세한 부분까지  제어
   ▷ 크기와 메모리가 작아 실행 속도가 빠름
3. 이식성이 좋음
   ▷ 별다른 수정없이 다양한 운영체제의 플랫폼에서 제공되는 컴파일러로 번역해 실행.
   ▷ 다양한 CPU와 플랫폼의 컴파일러를 지원.
 4. 다소 어려움
   ▷ C언어는 좀 어렵지만 한 번 익히면 다른 프로그래밍 언어 공부에도 도움이 됨.

C 언어를 배워야 하는 이유
1. 많은 언어에 영향을 미친 가장 기본이 되는 언어
    ▷C 언어를 알면 그 이후의 프로그래밍 언어들도 습득이 매우 쉬움.
2. 현장에서 다양한 분야에 사용되는 범용적인 언어 
    ▷임베디드 시스템, 응용프로그램, 운영체제와 같은 시스템 소프트웨어 개발등 여러 분야에 널리 사용.
3. 프로그래밍 지식과 프로그래밍 방법을 학습
    ▷자료형부터 메모리 할당까지 프로그래밍에 필요한 지식을 학습함.

# <2장> Visual Studio 설치

비주얼 스튜디오 : C/C++ 뿐만 아니라 C#, JavaScript, Python, Visual Studio 등의 여러 프로그램 언어를 이용하여 응용 프로그램을 개발 할 수 있는 플랫폼 개발 도구.

설치 과정

1.  비주얼 스튜디오를 검색하고 마이크로소프트 비주얼 스튜디오를 클릭.

2. 비주얼 스튜디오 홈페이지에서 
Window 사용하시는 분은 사진에서 왼쪽에서 Community를 다운로드 받으시고
Mac 사용하시는 분은 오른쪽 MacO 버전을 다운받으시면 됩니다.
저는 윈도우라서 윈도우 버전으로 받겠습니다.

3. 받고나서 파일을 열으시면 이런 창이 뜨는데 계속 눌러주세요.

4.워크로드입니다.
여기서는 C++을 사용한 데스크톱 개발을 체크하시고 오른쪽 밑에있는 Install을 클릭해주세요.
[꿀팁을 알려드리자면 비주얼스튜디오가 정말 무거워요... 조금이나마 덜 수 있는 방법이 설치위치 가셔서 IDE 설치위치를 외장하드로 바꿔도 잘 돌아가니 저처럼 컴퓨터에 저장공간이 없으신분은 추천드립니다. 저 방법으로 3GB정도 아낄 수 있어요. ]

5.이제 설치중입니다. 좀 무겁다보니 한 10분정도 다른거 하다가 오면 설치가 다 되어있을거에요.

6. 이제 비주얼 스튜디오가 열렸습니다. 새 프로젝트 만들기를 클릭하세요.

7. 빈 프로젝트를 클릭하고 다음버튼을 클릭해주세요.

8. 프로젝트 이름이나 위치를 정하는 곳입니다.
저는 그냥 하겠습니다.

9.이제 IDE가 열렸는데요. 소스파일에 우클릭 하시고 
추가 -> 새 항목을 클릭해주세요.

10.새 항목 추가 창에서 C++ 파일을 클릭해주시고
이름은  [짓고싶은 이름].c로 만들어 주세요.

11.c파일이 만들어 졌고, 아래의 문구를 그대로 입력해주세요.

#include <stdio.h>
int main(void) {
   printf("Hello World");
   return 0;
}
그리고 Ctrl + F5를 누르시면 실행이 됩니다.
결과는 이렇게 콘솔 창에 출력이 됩니다.


# <3장> 자료형 / 변수

## 프로그램 구조

<img src="https://postfiles.pstatic.net/MjAyMTA5MTdfMjM0/MDAxNjMxODUwNTcwNTIy.ImiX6pOAfKILnAoC15A79M9nCKf-LeggAvBJXUOnlDcg.xh_mJ_a_vk4IqBuSkCiWoMvX7xFgeEm08zkMsT2yqLQg.JPEG.wogur2689/%EC%A0%9C%EB%AA%A9%EC%9D%84_%EC%9E%85%EB%A0%A5%ED%95%B4%EC%A3%BC%EC%84%B8%EC%9A%94_-001.jpg?type=w773">

- 한 프로젝트는 단 하나의 함수 main()과 다른 여러 함수로 구현.
- 최종적으로 프로젝트 이름과 같은 하나의 실행파일이 제작.
- main()함수가 구현되어야 응용프로그램으로 실행됨.
- 실행 순서: main()함수 내에서 위에서 아래, 좌에서 우로, 문장이 위치한 순서대로 실행.

## 키워드
- 문법적으로 고유한 의미를 갖는 예약된 단어
- 프로그램 코드를 작성하는 사람이 이 단어들을 다른 용도로 사용금지.

## 식별자
- 프로그래머가 자기 스스로 정의해 사용하는 단어 (변수 이름, 함수 이름)
- 영문자, 숫자, 밑줄로 구성. 식별자의 첫문자로 숫자가 나올 수 없음.
- 키워드는 식별자가 될 수 없고, 대소문자를 구별하며, 중간에 공백문자를 포함하지 않음.
 
## 문장
- 프로그래밍 언어에서 컴퓨터에게 명령을 내리는 최소 단위
- 마지막에 세미콜론 ;으로 종료. (;를 빠뜨리면 문법오류 발생.)

## 블록과 들여쓰기
- 여러 개의 문자을 묶으면 블록, 블록 내부에서 문장들을 탭(tab)키로 오른쪽으로 들여쓰는 소스 작성 방식은 들여쓰기라고 한다.

```c
#include <stdio.h>

int main(void) 
{
  puts("C 언어");

  return 0;
}
```

들여쓰기가 잘된 코드

```c
#include <stdio.h>
int main(void) { puts("C 언어"); return 0;}
```

들여쓰기가 잘못된 코드


## 주석
- 프로그램 내용에는 전혀 영향을 미치지 않는 설명문
- 타인은 물론 자신에게도 필요하며, 주석에는 이 소스에 대한 설명을 적어 모든사람들을 이해시킴.
- //한줄주석 또는 /*블록 주석 */ 형식이 있음

## 자료형
- 프로그래밍 언어에서 자료를 식별하는 종류

<img src="https://postfiles.pstatic.net/MjAyMTA5MTdfMjIw/MDAxNjMxODUyNjA2MDI4.KTXrcWl9NOijFBtVB6T-ocEdVnLVPhke4fRENJbP4LIg.MHGs11TcYMNcGvZLsOCdeqjkA8wQF5KH-cCGoDQ9LWIg.JPEG.wogur2689/%EC%A0%9C%EB%AA%A9%EC%9D%84_%EC%9E%85%EB%A0%A5%ED%95%B4%EC%A3%BC%EC%84%B8%EC%9A%94_-001_(1).jpg?type=w773">

## 자료형의 분류 그림
- 기본형, 유도형, 사용자 정희형으로 나누어지고, 기본형은 정수형, 실수형, 문자형, void로 나누어짐.
- 프로그래머는 이러한 자료에 적당한 알고리즘을 적용해 프로그램을 작성.

## 변수
- 프로그래밍에도 정수와 실수같은 자료값을 저장하는 공간.
- 변수에는 고유한 이름이 붙여지며, 물리적으로 기억장치인 메모리에 위치
- 선언된 자료형에 따라 변수의 저장공간 크기와 저장되는 자료 값의 종류가 결정.
- 저장되는 값에 따라 변수 값은 바뀔 수 있고, 마지막에 저장된 하나의 값만 저장 유지.

```c
//자료형 변수이름
double height;

//여러 변수를 하나의 문장으로 선언
int width, height;
/*위 문장은 아래 문장과 같다.
* int width;
* int height;
*/
```
변수 선언문

## 대입
- 원하는 자료값을 선언된 변수에 저장
- 대입연산자 '=' : 오른쪽에 위치한 값을 왼쪽변수에 저장.

```c
int age;
age = 23;
age = 24;
// age란 변수에는 24라는 값이 저장됨.

//변수 초기화
int age = 20;
//변수 선언과 동시에 값을 저장.
```
