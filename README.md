# Tabel-Perkalian-dan-Pangkat-Akar-Kuadrat-dan-Kubik-
package Tabel;

/**
 * @author Azaria Dhea Rismaya
 */
import java.util.Scanner;

public class Tabel {
    
    public static void main(String[] args) {
        int perkalian,x,y; 
        Scanner masukan= new Scanner(System.in);
        System.out.println("Perkalian");
        System.out.print("Input nilai : ");
        perkalian = masukan.nextInt();
        System.out.print("x ");
        for(x=0;x<=perkalian;x++){
            System.out.print(x+"  ");
        }
        System.out.println("");
        for(x=0;x<=perkalian;x++){
            System.out.print(x+"  ");
            for(y=0;y<=perkalian;y++){
                System.out.print(y*x+ "  ");
            }
            System.out.println("");
        }
        System.out.println("");
        System.out.println("Pangkat Akar (Kuadrat dan Kubik)");
        System.out.println("  ");
        System.out.println("n\tKuadrat\tKubik\tAkarKuadrat\tAkarKubik");
        double a = 2.0,T = 0,b = 0.1,n,kuadrat,kubik,akarkuadrat,akarkubik;
        for(int p = 0; p <= 10; p++){
            n = a + T;
            T = T + b;
            for(int q = 0; q < 1; q++){
                kuadrat = Math.pow(n,2);
                for(int r = 0; r < 1; r++){
                    kubik = Math.pow(n,3);
                    for(int s = 0; s < 1; s++){
                        akarkuadrat = Math.sqrt(n);
                        for(int t = 0; t < 1; t++){
                            akarkubik = Math.cbrt(n);
                            System.out.println(n + "\t" 
                                    + String.format("%.3f",kuadrat) + "\t" 
                                    + String.format("%.3f",kubik) 
                                    + "\t" + String.format("%.3f",akarkuadrat) 
                                    + "\t\t" + String.format("%.3f",akarkubik));
                            System.out.println("");
                        }
                    }
                }
            }
        }
    }
}
