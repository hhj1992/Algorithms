# A / B 문제

## 문제

> 두 정수 A와 B를 입력받은 다음, A/B를 출력하는 프로그램을 작성하시오.

### 입력

> 첫째 줄에 A와 B가 주어진다. (0 < A, B < 10)

## 출력

> 첫째 줄에 A/B를 출력한다. 실제 정답과 출력값의 절대오차 또는 상대오차가 10-9 이하이면 정답이다.

```
1 / 3 = 0.33333333333333333333333333333333
4 / 5 = 0.8

```

## **문제 풀이**

### - Scanner 사용법

```java
import java.util.Scanner;

public class AdivisionB{
	
	public static void main(String[] args) {
		
		Scanner in = new Scanner(System.in);
		double A = in.nextDouble();
		double B = in.nextDouble();
		
		System.out.println(A / B);
		
		in.close();

	
	//float 플롯 = in.nextFloat();으로 했을때 틀렸습니다.
	
	
	}
}
```

- java.util.Scanner를 import 해서 ✨ Scanner 인스턴스 생성 ✨
- System.in 을 인자값으로 넣습니다. 
- >System.in → 입력값을 Byte 단위로 읽습니다 
- 변수에 담는다.
  (변수명은 가장 많이 쓰이는 in, scan, sc 등을 사용하는 것이 좋다.)
- 입력을 받아 값을 더해 출력한다.
- Scanner을 Close해준다.

### 참고코드

```java
// Reference Type
	// >> Class Type - String Class

		String 문자열_space = in.next();
        /*Space전까지의 문자열을 입력받는다. 에러발생경우 多*/

		String 문자열_Enter = in.nextLine();
		/*Enter전까지의 문자열을 입력받는다.*/


// Primitive Type
	// >> boolean Type

		boolean 부울 = in.nextBoolean();


	// >> Numeric Type
		// >> >> Integer Type

		byte 바이트 = in.nextByte();
		short 쇼트 = in.nextShort();
		int 정수 = in.nextInt();
		long 롱 = in.nextLong();



		// >> >> Floating Point Type

		double 더블형 = in.nextDouble();
		float 플롯 = in.nextFloat();
 
```

입력한 데이터가 변수 자료형에 위반되면 아래와 같은 에러가 뜬다.

`Exception in thread "main" java.util.InputMismatchException`
