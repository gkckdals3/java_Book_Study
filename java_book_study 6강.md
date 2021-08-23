# java_Book_Study
package java_practice6;

public class Tv {  
	String color;//색깔
	boolean power; //전원상태
	int channel;//채널
	
	void power() {power = !power;}// 켜기,끄기
	void channelUp() {channel++;}//볼륨 높이기
	void channelDown() {channel--;}//볼륨 낮추기

}

package java_practice6;

public class main {

	public static void main(String[] args) {
		Tv t;
		t = new Tv();
		t.channel=7;
		t.channelDown();
		System.out.println(t.channel);
		// TODO Auto-generated method stub

	}

}

package java_practice6;

public class main {

	public static void main(String[] args) {
		Tv t1 = new Tv();
		Tv t2 = new Tv();
		System.out.println("t1의 채널값은 "+t1.channel+"입니다.");
		System.out.println("t2의 채널값은 "+t2.channel+"입니다.");
		t2=t1;
		t1.channel=7;
		System.out.println("t1의 Channel값을 7로변경하였습니다.");
		
		System.out.println("t1의 channel값은"+t1.channel+"입니다.");
		System.out.println("t2의 channel값은"+t2.channel+"입니다.");

	}

}

package java_practice6;

public class main {

	public static void main(String[] args) {
		Tv[] tvArr = new Tv[3];
		
		for(int i=0; i<tvArr.length;i++)
		{
			tvArr[i] = new Tv();
			tvArr[i].channel=i+10;
		}
		for(int i=0;i<tvArr.length;i++)
		{
			tvArr[i].channelUp();
			System.out.printf("tvArr[%d].channel=%d%n",i,tvArr[i].channel);
			
		}

	}

}

package java_practice6;

public class Time {
	private int hour;
	private int minute;
	private float second;
	
	public int gethour() {return hour;}
	public int getminute() {return minute;}
	public float getsecond() {return second;}

	public void sethour(int h)
	{
		if(h<0||h>23) return;
		hour=h;
	}
	public void setminute(int m)
	{
		if(m<0||m>59) return;
		minute=m;
	}
	public void setsecond(float s)
	{
		if(s<0.0f||s>59.99f) return;
		second=s;
	}
	
}

package java_practice61;

public class CardTest {

	public static void main(String[] args) {
		System.out.println("Card.width = "+Card.width);
		System.out.println("Card.height = "+Card.height);
		
		Card c1 = new Card();
		c1.kind = "Heart";
		c1.number='7';
		
		Card c2 = new Card();
		c2.kind = "Spade";
		c2.number = '3';
		
		System.out.println(c1.kind,c1.number,c1.width,c1.height);
		System.out.println(c2.kind,c2.number,c2.width,c2.height);
		c1.width=50;
		c1.height=80;
		
		System.out.println(c1.kind,c1.number,c1.width,c1.height);
		System.out.println(c2.kind,c2.number,c2.width,c2.height);
		// TODO Auto-generated method stub

	}

}

package java_practice62;

public class primitiveParamEX {

	public static void main(String[] args) {
		Data d= new Data();
		d.x=10;
		System.out.println("main() : x = "+d.x);
		
		change(d.x);
		System.out.println("After change(d.x)");
		System.out.println("main() : x = "+d.x);
		// TODO Auto-generated method stub

	}
	static void change (int x)
	{
		x=1000;
		System.out.println("change() : x =" + x);
	}

}

package java_practice63;
public class main{

	public static void main(String[] args) {
		int [] arr = new int[] {3,2,1,6,5,4};
		
		printArr(arr);
		sortArr(arr);
		printArr(arr);
		System.out.println(sumArr(arr));
		// TODO Auto-generated method stub

	}

	static void printArr(int arr[])
	{
		System.out.print('[');
		for(int i : arr)
			System.out.print(i+",");
		System.out.println(']');
		
	}
	
	static void sortArr(int arr[])
	{
		for(int i=0;i<arr.length-1;i++)
			for(int j=0;j<arr.length-1-i;j++)
				if(arr[j]>arr[j+1]) 
				{
					int temp = arr[j];
					arr[j]=arr[j+1];
					arr[j+1]=temp;
				}
		
	}
	static int sumArr(int arr[])
	{
		int sum=0;
		for(int i=0;i<arr.length;i++)
		{
			sum+=arr[i];
		}
		return sum;
	}
}

package java_practice63;
public class main{

	public static void main(String[] args) {

		int x=2;
		int n=5;
		int result=0;
		
		for(int i=1;i<=n;i++)
		{
			result+=power(x,i);
		}
		System.out.println(result);
		
}
	
	static int power(int x,int n)
	{
		if (n==1)
			return x;
		return x*power(x,n-1);
	}
g}





