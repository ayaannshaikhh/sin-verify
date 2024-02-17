## This code was created as an assignment for ICS4UA: AP Computer Science.
### Language: Java
```java
// Class is called socialinsurancenumber
package socialinsurancenumber;

import java.util.Scanner;

public class SocialInsuranceNumberVerifier {

	public static void main(String[] args) {
		String province = "x";
		Scanner scanner = new Scanner(System.in);
		System.out.println("+ SOCIAL INSURANCE NUMBER VERIFIER +\n\nThis system will verify whether or not your SIN number is valid.\n\nTo begin, enter the 9 digits of your SIN number, WITHOUT SPACES.");
		
		String sinNumber = scanner.nextLine();
		
		if (sinNumber.length() != 9) {
			System.out.println("The SIN number that was inputted is not valid. Please try again!");
		}
		
		if (sinNumber.startsWith("1")) {
			province = "New Brunswick, Newfoundland and Labrador, Nova Scotia, Prince Edward Island";
		} else if (sinNumber.startsWith("2")) {
			province = "Quebec";
		} else if (sinNumber.startsWith("3")) {
			province = "Quebec";
		} else if (sinNumber.startsWith("4")) {
			province = "Ontario";
		} else if (sinNumber.startsWith("5")) {
			province = "Ontario";
		} else if (sinNumber.startsWith("6")) {
			province = "Alberta, Manitoba, Saskatchewan, Northwest Territories, Nunavut";
		} else if (sinNumber.startsWith("7")) {
			province = "British Columbia, Yukon";
		} else if (sinNumber.startsWith("8")) {
			System.out.println("This SIN Number is not valid.");
		} else if (sinNumber.startsWith("9")) {
			province = "No Province [Immigrant and/or Temporary SIN Card]";
		} else if (sinNumber.startsWith("0")) {
			System.out.println("This SIN Number is not valid.");
		}
		
		// Using an array to split the digits into individual strings so I can do a calculation
		String[] sinDigits = sinNumber.split("");
		
		// Converting string to Int
		int one = Integer.parseInt(sinDigits[0]);
		int two = Integer.parseInt(sinDigits[1]);
		int three = Integer.parseInt(sinDigits[2]);
		int four = Integer.parseInt(sinDigits[3]);
		int five = Integer.parseInt(sinDigits[4]);
		int six = Integer.parseInt(sinDigits[5]);
		int seven = Integer.parseInt(sinDigits[6]);
		int eight = Integer.parseInt(sinDigits[7]);
		int nine = Integer.parseInt(sinDigits[8]);
		
		one = one * 1;
		two = two * 2;
		three = three * 1;
		four = four * 2;
		five = five * 1;
		six = six * 2;
		seven = seven * 1;
		eight = eight * 2;
		nine = nine * 1;
		
		if(one >= 10) {
			int digit1 = one % 10;
			int digit2 = one / 10;
			one = digit1 + digit2;
		}
		
		if(two >= 10) {
			int digit3 = two % 10;
			int digit4 = two / 10;
			two = digit3 + digit4;
		}
		
		if(three >= 10) {
			int digit5 = three % 10;
			int digit6 = three / 10;
			three = digit5 + digit6;
		}
		
		if(four >= 10) {
			int digit7 = four % 10;
			int digit8 = four / 10;
			
			four = digit7 + digit8;
		}
		
		if(five >= 10) {
			int digit9 = five % 10;
			int digit10 = five / 10;
			five = digit9 + digit10;
		}

		if(six >= 10) {
			int digit11 = six % 10;
			int digit12 = six / 10;
			six = digit11 + digit12;
		}
		
		if(seven >= 10) {
			int digit13 = seven % 10;
			int digit14 = seven / 10;
			seven = digit13 + digit14;
		}
		
		if(eight >= 10) {
			int digit15 = eight % 10;
			int digit16 = eight / 10;
			eight = digit15 + digit16;
		}
		
		if(nine >= 10) {
			int digit17 = nine % 10;
			int digit18 = nine / 10;
			nine = digit17 + digit18;
		}
		
		int sum = one + two + three + four + five + six + seven + eight + nine;
 		sum = sum % 10;
		
		
		if (sum != 0) {
			System.out.println("The inputted social security number is not valid. Please input it again.");
		} else
			System.out.println("\nProvince: " + province + "\nYour social security number is valid! Congratulations! :)");
	
		
	}

}
```
