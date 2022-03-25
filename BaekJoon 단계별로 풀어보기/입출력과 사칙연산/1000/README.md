# A+B 문제

## 문제

> 두 정수 A와 B를 입력받은 다음, A+B를 출력하는 프로그램을 작성하시오.

## 입력

> 첫째 줄에 A와 B가 주어진다. (0 < A, B < 10)

## 출력

```
2 + 3 = 5
4 + 9 = 13
```

### 문제 풀이

```java
import java.util.Scanner;

public class AplusB {

    public static void main(String[] args) {

        Scanner in = new Scanner(System.in);
        int A = in.nextInt();
        int B = in.nextInt();

        System.out.println(A + B);

        in.close();
    }

}
```

- java.util.Scanner를 import 한다.
- 입력한 값을 Byte 단위로 읽는 System.in을 인자값으로 넣어 Scanner 인스턴스를 생성하여
  변수에 담는다. 변수명은 가장 많이 쓰이는 in, scan, sc 등을 사용하는 것이 좋다.
- 입력을 받아 값을 더해 출력한다.
- SCanner을 Close해준다.

`참고 코드`

```java
// Reference Type
	// >> Class Type - String Class

		String 문자열_space = in.next();
        /*Space전까지의 문자열을 입력받는다.*/

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
