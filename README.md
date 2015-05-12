# Factorials
CS3 assignment (Dalton)

public class Factorials {
	/*
	@author Raina
	 */



	//Base case- 0!=1    Recursive step= x!=x*(x-1)! --> 5!=5*4!  4!=4*3!  3!=3*2! 2!=2*1! 1!=1*0! 0!=1 --> 5!=5*24

	static int factorial(int num) {
		int fact = 1;
		while (num>0){
			fact*=num--;
		}
		return fact;
	}
	static int factorialR(int num){

		if (num==0) return 1;
		return num * factorialR(num-1);
	}

	static int sumR(int num){
		if (num==0) return 0;
		return sumR(num-1) + num;

	}

	static int poweR(int num, int a){
		if (a==0) return 1;
		return num*poweR(num,a-1);
	}

	static int fibonacci(int num){
		if (num==0) return 0;
		else if (num==1) return 1;
		return fibonacci(num-1)+fibonacci(num-2);
	}

	static int sumdigit(int num){
		if (num<10) return num;
		return (num/10)+num%10;
	}

	static int prodigit(int num){
		if (num<10) return num;
		return (num/10)*num%10;
	}

	static int multiplyR(int num, int a){
		if (a==0) return 0;
		//else if (a<num) return (int a,int num);
		return num+multiplyR(num,a-1);
	}

	static int sumrange(int num, int a){
		if (num==a) return num;
		else if (a==0) return num;
		return a+sumrange(num,a-1); 
	}

	static int digreverse(int num, int a){
		if (num<10) return num+10*a;
		return digreverse(num/10,10*a+num%10);
	}

	static int gcd(int num, int a){
		if (a<=num && num%a==0) return a;
		return gcd(a,num%a);
	}

	static int compint(int num, int a, int b){
		if (b==0) return num;
		return (a+1)*compint(num,a,b-1);
	}

	static int sqroot(int num, int a, int b){
		if (Math.abs(b^2-num)<a) return b;
		return sqroot(num,a,(b+num/b)/2);
	}

	// static int sr(int num, int a, int b, int c){

	//  }

	static int combo(int num, int a){
		if (a==1) return num;
		else if (a>num) return 0;
		else if (a==num) return 1;
		return combo(num-1,a)+combo(num-1, a-1);
	}

	public static void main(String args[]){
		int num = Integer.parseInt(args[0]);
		int a = Integer.parseInt(args[1]);
		int b = Integer.parseInt(args[2]);
		int c= Integer.parseInt(args[3]);


		System.out.println(factorialR(num));
		System.out.println(sumR(num));
		System.out.println(poweR(num,a));
		System.out.println(fibonacci(num));
		System.out.println(sumdigit(num));
		System.out.println(prodigit(num));
		System.out.println(multiplyR(num,a));
		System.out.println(sumrange(num,a));
		System.out.println(digreverse(num,a));
		System.out.println(gcd(num,a));
		System.out.println(compint(num, a, b));
		System.out.println(sqroot(num, a, b));
		//System.out.println(sr(num, a, b, c));
		System.out.println(combo(num,a));
	}
}

