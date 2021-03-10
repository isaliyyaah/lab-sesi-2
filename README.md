# lab-sesi-2
package com.company;

import java.util.Scanner;
import java.text.DecimalFormat;
import java.util.Random;

public class Main
{
    public static void main(String[] args)
    {
		Random in = new Random();
		int random1 = in.nextInt(9 - 0);
		int random2 = in.nextInt(9 - 0);
		int x, go1, go2;

		Scanner put = new Scanner (System.in);
	    DecimalFormat For = new DecimalFormat("00");

	    System.out.println("angka random: " + random1 + "" + random2);

	    System.out.println("input angka: ");
		x = put.nextInt();
		if (x >99) {
			System.out.println("it's over");
		} else {
			String inputFor = For.format(x);

			go1 = Character.getNumericValue(inputFor.charAt(0));
			go2 = Character.getNumericValue(inputFor.charAt(1));

			if (go1 == random1 && go2 == random2) {
				System.out.println("you got $10.000");
			} else if (go1 == random2 && go2 == random1) {
				System.out.println("you got $3.000");
			} else if (go1 == random1 || go2 == random2 || go1 == random2 || go2 == random1) {
				System.out.println("you got $1.000");
			} else {
				System.out.println("try again");
			}
		}
    }
}
