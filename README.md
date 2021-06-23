# java-1
import java.util.Random;

public class Die {
	int value;
	Random random = new Random();
	int roll() {//주사위를 던진다
		value = random.nextInt(6);
		value +=1;
		return value;
	}

}
import java.util.*;//Random 클래스를 포함

public class MyDie2 {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		int i;
		
		newDie a = new newDie();//정의된 주사위 생성
		i=a.roll();//주사위 실행
		System.out.println("die = " +i);
		

	}

}

public class newDie extends Die {
	int i;
	int roll() {
		i=super.roll();
		if(i<=3)
			return i;
		else if(i%3==0)
			return i;
		else {
			i=roll();
			return i;
		}
		
	}

}
