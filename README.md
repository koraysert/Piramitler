# Piramitler
DiziVeTekDöngü
package piramit.base;

import java.util.Arrays;
import java.util.Scanner;

public class Runner {

	static Scanner scn = new Scanner(System.in);
	static String girilen;
	static String s;

	public static void main(String[] args) {
		
		while (girilen !="") {
			System.out.println("sayı giriniz");
			getir();
		  piramit(Integer.parseInt(girilen));
		  piramitsag(Integer.parseInt(girilen));
		  piramitsol(Integer.parseInt(girilen));
			piramitters(Integer.parseInt(girilen));
				
		}
		
	}

	public static String getir() {
		girilen = scn.next();
		return girilen;
	}

	public static void piramit(int sayi) {
		if (sayi % 2 == 1) {
			char[] d = new char[sayi];
			for (int i = 0; i <= sayi / 2; i++) {
				d[((sayi - 1) / 2) - i] = 'x';
				d[((sayi - 1) / 2) + i] = 'x';
				s = new String(d);
				System.out.println(s);
			}

		} else {
			sayi = sayi + 1;
			char[] d = new char[sayi];
			for (int i = 0; i <= sayi / 2; i++) {
				d[((sayi - 1) / 2) - i] = 'x';
				d[((sayi - 1) / 2) + i] = 'x';
				s = new String(d);
				System.out.println(s);
			}
		}

	}

	public static void piramitsag(int sayi) {
		
		if (sayi % 2 == 1) {
			char[] d = new char[sayi];
			for (int i = 0; i < sayi; i++) {

				if (i > (sayi - 1) / 2) {
					d[sayi - i] = ' ';
					s = new String(d);
					System.out.println(s);
				} else {
					d[i] = 'x';
					s = new String(d);
					System.out.println(s);
				}

			}

		} else {	sayi=sayi+1;	char[] d = new char[sayi];
		for (int i = 0; i < sayi; i++) {

			if (i > (sayi - 1) / 2) {
				d[sayi - i] = ' ';
				s = new String(d);
				System.out.println(s);
			} else {
				d[i] = 'x';
				s = new String(d);
				System.out.println(s);
			}

		}
		}

	}
	
	public static void piramitters(int sayi) {
	if (sayi % 2 == 1) {

		String[][] d = new String[sayi][sayi];
		String s1="";
		String s2="";
		
			for(int i =0;i<(sayi+1)/2;i++) {
				for(int j=0;j<(sayi+1)/2;j++) {
					
				if(j>=i) {d[i][j]="x";}
				else {d[i][j]=" ";}
				s1+=d[i][j];
				
				//System.out.print(d[i][j]);
				
				}
				for(int k=s1.length()-1;k>=0;k--) {s2+=s1.toCharArray()[k];}
//				char tempArray[] = s1.toCharArray();
//				Arrays.sort(tempArray);
//				s2=new String(tempArray);
				System.out.println(s1+s2);
				s1="";
				s2="";
			
			
			}
	} 

	else {sayi=sayi+1;		
	String[][] d = new String[sayi][sayi];
	String s1="";
	String s2="";
	
		for(int i =0;i<(sayi+1)/2;i++) {
			for(int j=0;j<(sayi+1)/2;j++) {
				
			if(j>=i) {d[i][j]="x";}
			else {d[i][j]=" ";}
			s1+=d[i][j];
			
			//System.out.print(d[i][j]);
			
			}
			for(int k=s1.length()-1;k>=0;k--) {s2+=s1.toCharArray()[k];}
//			char tempArray[] = s1.toCharArray();
//			Arrays.sort(tempArray);
//			s2=new String(tempArray);
			System.out.println(s1+s2);
			s1="";
			s2="";
		
		
		}}
		
	}
	
	public static void piramitsol(int sayi) {
		if (sayi % 2 == 1) {
			char[] d = new char[sayi];
			for (int i = sayi-1; i >=0; i--) {

				if (i > (sayi - 1) / 2-1) {

					d[i-((sayi - 1) / 2)] = 'x';
					s = new String(d);
					System.out.println(s);
				} else {
					d[((sayi - 1) / 2) - i-1] = ' ';
					s = new String(d);
					System.out.println(s);
					
				}

			}

		} else {	sayi=sayi+1;	
		char[] d = new char[sayi];
		for (int i = sayi-1; i >=0; i--) {

			if (i > (sayi - 1) / 2-1) {

				d[i-((sayi - 1) / 2)] = 'x';
				s = new String(d);
				System.out.println(s);
			} else {
				d[((sayi - 1) / 2) - i-1] = ' ';
				s = new String(d);
				System.out.println(s);
				
			}

		}
		}

	}
}
