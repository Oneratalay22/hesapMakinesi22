import java.util.Scanner;

public class Main {
    static int sum(int a, int b) {
        int result = a + b;
        System.out.println("Toplam :" + result);
        return result;
    }

    static int minus(int a, int b) {
        int result = a - b;
        System.out.println("Çıkarma :" + result);
        return result;

    }

    static int times(int a, int b) {
        int result = a * b;
        System.out.println("Çarpma:" + result);
        return result;
    }

    static int divided(int a, int b) {
        int result = a / b;
        System.out.println("Bölme:" + result);
        return result;
    }

    static int power(int a, int b) {
        int result = 1;
        for (int i = 1; i <= b; i++) {
            result *= a;
        }
        return result;
    }

    static int factorial(int a, int b) {
        return a % b;
    }

    static int mod(int a, int b) {
        int result = a % b;
        return result;
    }

    static void calc(int a, int b) {
        System.out.println("Çevresi:" + (2 * (a + b)));
        System.out.println("Alanı:" + (a + b));

    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int select;

        String menu = "1- Toplama\n"
                + "2-Çıkarma\n"
                + "3-Çarpma\n"
                + "4-Bölme\n"
                + "5-Üslü sayı\n"
                + "6-Mod almak\n"
                + "7-Dikdörtgen Alan ve Çevre Hesabı\n"
                + "0-Çıkış yap";
        System.out.println(menu);
        while (true) {
            System.out.println("Bir işlem seçiniz!:");
            select = sc.nextInt();
            if (select == 0) {
                break;
            }
            System.out.println("İlk Sayı:");
            int a = sc.nextInt();
            System.out.println("İkinci Sayı:");
            int b = sc.nextInt();
            switch (select) {
                case 1:
                    sum(a, b);
                    break;
                case 2:
                    minus(a, b);
                    break;
                case 3:
                    times(a, b);
                    break;
                case 4:
                    divided(a, b);
                    break;
                case 5:
                    System.out.println("Üs Hesabı" + power(a, b));
                    break;
                case 6:
                    System.out.println("Mod İşlemi:" + mod(a, b));
                    break;
                case 7:
                    calc(a, b);
                    break;
                default:
                    System.out.println("Geçersiz bir işlem girdiniz:");

            }
            System.out.println("Görüşmek üzere");

        }

    }
}
