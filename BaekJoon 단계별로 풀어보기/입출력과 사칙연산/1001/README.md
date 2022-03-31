# A+B 문제

## 문제

> 두 정수 A와 B를 입력받은 다음, A-B를 출력하는 프로그램을 작성하시오.

### 입력

> 첫째 줄에 A와 B가 주어진다. (0 < A, B < 10)

### 출력

```
10 - 5 = 5
20 - 1 = 19
```

## **문제 풀이**

### - Scanner 사용법

```java
import java.util.Scanner;

public class AminusB {

    public static void main(String[] args) {

        Scanner in = new Scanner(System.in);
        int A = in.nextInt();
        int B = in.nextInt();

        System.out.println(A - B);

        in.close();
    }

}
```

- java.util.Scanner를 import 한다.
- 입력한 값을 Byte 단위로 읽는 System.in을 인자값으로 넣어 Scanner 인스턴스를 생성하여
  변수에 담는다.  
  (변수명은 가장 많이 쓰이는 in, scan, sc 등을 사용하는 것이 좋다.)
- 입력을 받아 값을 빼서 출력한다.
- Scanner을 Close해준다.

### - BufferedReader 사용법

    BufferedReader.read() : 한 문자를 읽는다.
    BufferedReader.readLine() : 한 행을 읽는다.

##### 1.StringTokenizer("Parsing할 문자열", 구분자) 이용

```java
import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;
import java.util.StringTokenizer;

public class AminusB {

	public static void main(String[] args) throws IOException {

		BufferedReader br = new BufferedReader(new InputStreamReader(System.in));

 		String str = br.readLine();
		StringTokenizer st = new StringTokenizer(str," ");

        /*읽는 것과 동시에 구분자값으로 넣어줄 수 있다.
        StringTokenizer st = new StringTokenizer(br.readLine()," ");*/

		int a = Integer.parseInt(st.nextToken());

		int b = Integer.parseInt(st.nextToken());

		System.out.println(a-b);

    }
}
```

- 키보드로 입력된 값을 InputStreamReader로 읽고 BufferedReader에 차곡차곡 담아 변수 br에 넣는다.
- br을 한줄씩 읽어서 str에 담는다
- StringTokenizer 인스턴스를 생성해서 지정된 구분자로 한줄씩 읽은 문자열 str을 Parsing해서 st에 담는다
- nextToken()은 구분된 문자열을 반환해준다. Integer.parseInt로 int로 바꿔준다.

##### 2.split(구분자) 이용

```java

import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;

public class AminusB {

	public static void main(String[] args) throws IOException {

		BufferedReader br = new BufferedReader(new InputStreamReader(System.in));

		String[] str = br.readLine().split(" ");
		int a = Integer.parseInt(str[0]);
		int b = Integer.parseInt(str[1]);

		System.out.println(a-b);

	}

}
```

- 키보드로 입력된 값을 InputStreamReader로 읽고 BufferedReader에 차곡차곡 담아 변수 br에 넣는다.
- br을 한줄씩 읽고 split 구분자 기준으로 Parsing해서 String [] str에 담는다
- Array에서 하나씩 꺼내서 Integer.parseInt로 int로 바꿔준다.

`데이터 양이 많아지게 되면 StringTokenizer 보다 split이 성능이 낮아 수행시간 차이가 발생한다.`

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
