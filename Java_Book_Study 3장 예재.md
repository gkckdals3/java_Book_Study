# java_Book_Study
package java_practice21;

public class main {

	public static void main(String[] args) {
        int x = 2;
        int y = 5;
        char c = 'A';

        System.out.println(1 + x << 33); // int형은 총 32비트이므로 33비트만큼 쉬프트를 진행하면 결국 1비트만큼 움직인 것과 같다. 그러므로 110(2)이므로 정답은 6이다.
        System.out.println(y >= 5 || x < 0 && x > 2); //or 연산자이므로 true
        System.out.println(y += 10 - x++); // 15-2=13 x++은 다음줄부터 적용
        System.out.println(x += 2); // 5
        System.out.println(!('A' <= c && c <= 'Z')); // 괄호안의 값은true 이지만 부정연산자가 있으므로 false 
        System.out.println('C' - c); // 2 
        System.out.println('5' - '0'); // 5 
        System.out.println(c + 1); // B
        System.out.println(++c); // B
        System.out.println(c++); // B
        System.out.println(c); // C
		
		// TODO Auto-generated method stub

	}

}

package java_practice22;

public class main {

	public static void main(String[] args) {
		//아래의 코드는 사과를 담는데 필요한 바구니(버켓)의 수를 구하는 코드이다. 만일 사과의 수가 123개이고 하나의 바구니에는 10개의 사과를 담을 수 있다면, 13개의 바구니가 필요할 것이다. (1)에 알맞은 코드를 넣으시오.
		int apple = 123;
		int bucket= 10;
		int spare= apple/bucket+(apple%bucket>0 ? 1:0);
		System.out.println("필요한 바구니의 양은"+ spare +"개 입니다.");
		// TODO Auto-generated method stub

	}

}
package java_practice23;
import java.util.Scanner;

public class main {

	public static void main(String[] args) {
		// 아래는 변수 num의 값 중에서 일의 자리를 1로 바꾸는 코드이다. 만일 변수 num의 값이 333이라면 331이 되고, 777이라면 771이 된다.
	   
		System.out.println("세자리 정수를 입력하시오.");
		Scanner sc = new Scanner(System.in);
	   int num=sc.nextInt();
	   int Result= num/10*10+1;
	   System.out.println(Result);

	}

}

package java_practice24;
import java.util.Scanner;

public class main {

	public static void main(String[] args) {
		// 아래는 변수 num의 값보다 크면서도 가장 가까운 10의 배수에서 변수 num의 값을 뺀 나머지를 구하는 코드이다. 예를 들어, 24의 크면서도 가장 가까운 10의 배수는 30이다. 19의 경우 20이고, 81의 경우 90이 된다. 30에서 24를 뺀 나머지는 6이기 때문에 변수 num의 값이 24라면 6을 결과로 얻어야 한다.

		Scanner sc = new Scanner(System.in);
		int num=sc.nextInt();
		int k= num/10*10+10;
		int result = k-num;
		System.out.println("정답은 "+result);
		
	}

}

package java_practice210;
import java.util.Scanner;

public class main {

	public static void main(String[] args) {
		//3-10. 다음은 대문자를 소문자로 변경하는 코드인데, 문자 ch에 저장된 문자가 대문자인 경우에만 소문자로 변경한다. 문자코드는 소문자가 대문자보다 32만큼 더 크다. 예를 들어 'A'의 코드는 65이고, 'a'의 코드는 97이다. 알맞은 코드를 넣으세요.
		Scanner sc= new Scanner(System.in);
		int chI = sc.nextInt();
		if(chI>=65 && chI<97)
		{
			System.out.printf("%d의 값은 %c입니다.",chI,chI+32);
		}
		else if(chI>=97)
		{
			System.out.printf("%d의 값은 %c입니다.",chI,chI);
		}
		else
		{
			System.out.println("잘못된 수 입니다.");
		}
			
		// TODO Auto-generated method stub

	}

}
