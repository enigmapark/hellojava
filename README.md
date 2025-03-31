

import java.util.Scanner;

public class Problem07 {
 public static void main(String [] args) {
	 
	 Scanner sc = new Scanner(System.in);
	 String inputNum = "";
	 boolean cont = true ;
	 
	 System.out.println("==============");
	 System.out.println("[ 숫자 맞추기 게임 ] ");
	 System.out.println("==============");
	
	 
	 while(cont) {
	
		 int random = (int)(Math.random() * 100 ) + 1 ;
		 
		 System.out.println(random); 
	 
	 while(true) { 
	 System.out.print(">>");
	 inputNum = sc.nextLine();
	 if(random > Integer.parseInt(inputNum)) {
		 System.out.println("더 높게 ");
	 } else if(random < Integer.parseInt(inputNum)) {
		 System.out.println("더 낮게 ");
		 
	 } else {
		 System.out.println("맞았습니다") ;
		 break ; 
	 } 
 }
	 System.out.println("게임을 종료 하시겠습니까? (y/n") ;
	 inputNum = sc.nextLine();
	 if("y".equals(inputNum) || "y".equals(inputNum)) {
		 cont = false;
	 }else {
		 cont = true;
		 
	 }
	 }
 }
}
	 
	 

