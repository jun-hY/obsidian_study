
### C의 출력

콘솔창에서 출력이 나옴

```cpp
#include <stdio.h> // standard input output -> 표준 입출력 장치

void main() // 프로그램에 시작알리는 main 함수
{
    printf("Hello, World!\n"); // C언어 콘솔에 출력하기 위한 함수
}
```

### C에서 특수 문자 출력하기.

ASCII 코드로 문자를 받는다 한글은 유니코드

### C의 입력

```c
#include <stdio.h>

void main()
{
    int a = 0;         // 입력할 저장할 변수 선언
    scanf("%d", &a);   // 입력을 받는 함수
    printf("%d\n", a); // 출력하는 함수
}
```

