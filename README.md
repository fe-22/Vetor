# Vetor
Reserva de produtos em estoque, calculo total do custo e plano de pagamento em 10X. 
package application;

import java.util.Locale;
import java.util.Scanner;

import entities.Product;

public class Program {

	public static void main(String[] args) {
		
		Locale.setDefault(Locale.US);
		Scanner sc = new Scanner(System.in);
		
		int n = sc.nextInt();
		Product [] vect = new Product[n];
		
		for (int i=0; i< n; i ++) {
			sc.nextLine();
			String name = sc.nextLine();
			double price = sc.nextDouble();
			vect[i] = new Product(name, price);
		}

		double sum = 0.0;
		       for (int i=0; i< n; i++) {
		       sum += vect[i].getPrice();  
		       }
		       
		   
		       double avg = sum / 10;
		       double soma = sum ++ ;
		       
		       System.out.printf("total =R$%.2f%n",soma);
		       System.out.printf("parcelamento 10x =R$%.2f%n",avg);
		       
		       sc.close();
	}
  
	  
}
