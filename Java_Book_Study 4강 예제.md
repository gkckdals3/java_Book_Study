# java_Book_Study
package java_practice31;

public class main {

	public static void main(String[] args) {
		int sum =0;
		//1부터 20까지의 정수 중에서 2 또는 3의 배수가 아닌 수의 총합을 구하시오.
	for (int i =1;i<=20;i++)
	{
		if(i%2!=0 && i%3!=0)
		{
			sum+=i;
		}
	}
	System.out.println(sum);
	}

}

package java_practice32;

public class main {

	public static void main(String[] args) {
		//4-3. 1+(1+2)+(1+2+3)+(1+2+3+4)+...+(1+2+3+...+10)의 결과를 계산하시오.
		int sum=0;
		for(int j=1;j<11;j++)
		{
			for(int i=1;i<11;i++)
			{
				sum+=i;
			}
		}
		// TODO Auto-generated method stub

		System.out.println(sum);
	}

}

package java_practice33;

public class main {

	public static void main(String[] args) {
		//4-4. 1+(-2)+3+(-4)+... 과 같은 식으로 계속 더해나갔을 때, 몇까지 더해야 총합이 100이상이 되는지 구하시오.
		int sum=0;
		for(int i=1;;i++)
		{
			if(i%2==0)
			{
				sum-=i;
			}
			else
			{
				sum+=i;
			}
			if(sum>=100) {
				System.out.println(i);
			    break;
			}
			
		}
		


		// TODO Auto-generated method stub

	}

}

package java_practice34;

public class main {

	public static void main(String[] args) {
		//다음의 for문을 while문으로 변경하시오.
		/*public class Exercise4_5 {
    public static void main(String[] args) {
        for(int i=0; i<=10; i++) {
            for(int j=0; j<=i; j++)
                System.out.print("*");
            System.out.println();
        }
    } // end of main
} // end of class*/
		int i=0;
		while(i<=10)
		{
			int j=0;
			while(j<=i)
			{
				System.out.print("*");
				j++;
			}
			System.out.println("");
			i++;
		}
		
		// TODO Auto-generated method stub

	}

}

package java_practice35;

public class main {

	public static void main(String[] args) {
		//4-6. 두 개의 주사위를 던졌을 때, 눈의 합이 6이 되는 모든 경우의 수를 출력하는 프로그램을 작성하시오.
		for(int i=1;i<=6;i++)
		{
			for(int j=1;j<=6;j++)
			{
				if(i+j==6)
				{
					System.out.printf("경우의수 %d와%d",i,j);
					System.out.println("");
				}
			}
		}
		// TODO Auto-generated method stub

	}

}

package java_practice36;

public class main {

	public static void main(String[] args) {
		//Math.random()을 이용해서 1부터 6사이의 임의의 정수를 변수 value에 저장하는 코드를 완성하라.
		int value=(int)(Math.random()*6+1);
		System.out.println(value);
		// TODO Auto-generated method stub

	}

}








