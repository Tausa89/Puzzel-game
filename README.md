# Puzzel-game
import java.util.Scanner;
import java.util.Random;
import java.util.concurrent.TimeUnit;


public class Zmienne2 {

    public static void main(String args[]) throws InterruptedException {

        //Program losuje liczbe
        Scanner odczyt = new Scanner(System.in);

        Random losowa = new Random();

        System.out.println("Witam w naszej grze. Program wylosuje dla Ciebie liczbę " +
                "w zakresie od 1 do 1000 a Ty bedziesz musiał ja zgadnać");

        System.out.println("Program losuje liczbę. Proszę czekać.");

        int liczba = losowa.nextInt(1000);

        TimeUnit.SECONDS.sleep(2);

        System.out.println("OK. Liczba zostałą wylosowan spróbuj ją teraz zgadnać.");

        int liczbaProb = 0;


        while (true) {

            int typowanaLibcza = Integer.parseInt(odczyt.nextLine());

            liczbaProb++;


            if (typowanaLibcza>liczba){
                System.out.println("Twoja liczba jest za duża");
            } else if (typowanaLibcza<liczba) {
                System.out.println("Twoja libcza jest za mała");
            } else if (typowanaLibcza==liczba) {
                System.out.println("Brawo!!! Zgadłeś Twoja liczba to " + typowanaLibcza);
                break;
            }

        }

        System.out.println("Liczba która wylosował system to "+liczba);
        if (liczbaProb<10){
            System.out.println("Udało Ci się zgadnać za "+ liczbaProb + " razem. Gratulacje to super wynik!!!");
        } else {
            System.out.println("Udało Ci się zgadnać za "+ liczbaProb + " razem. Myślę że możesz postarać się bardziej.");
        }



    }
}
