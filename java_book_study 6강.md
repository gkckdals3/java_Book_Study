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


