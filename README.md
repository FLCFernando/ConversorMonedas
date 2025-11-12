import java.util.Scanner;

class ConversorMonedas {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int opcion;
        double cantidad;

        // Tasas de cambio aproximadas (puedes modificarlas)
        double dolarAPesoArg = 1409.99;
        double dolarAReal = 5.27;
        double dolarAPesoCol = 3752.94;

        do {
            System.out.println("=====================================");
            System.out.println("        CONVERSOR DE MONEDAS");
            System.out.println("=====================================");
            System.out.println("1) Dólar a Peso Argentino");
            System.out.println("2) Peso Argentino a Dólar");
            System.out.println("3) Dólar a Real Brasileño");
            System.out.println("4) Real Brasileño a Dólar");
            System.out.println("5) Dólar a Peso Colombiano");
            System.out.println("6) Peso Colombiano a Dólar");
            System.out.println("7) Salir del programa");
            System.out.print("Elige una opción: ");

            // Validación para que el usuario no escriba texto
            while (!sc.hasNextInt()) {
                System.out.println("Por favor, ingresa un número válido.");
                sc.next(); // descarta la entrada incorrecta
                System.out.print("Elige una opción: ");
            }

            opcion = sc.nextInt();

            switch (opcion) {
                case 1:
                    System.out.print("Ingresa la cantidad en dólares: ");
                    cantidad = sc.nextDouble();
                    System.out.println("Equivale a " + (cantidad * dolarAPesoArg) + " pesos argentinos.\n");
                    break;
                case 2:
                    System.out.print("Ingresa la cantidad en pesos argentinos: ");
                    cantidad = sc.nextDouble();
                    System.out.println("Equivale a " + (cantidad / dolarAPesoArg) + " dólares.\n");
                    break;
                case 3:
                    System.out.print("Ingresa la cantidad en dólares: ");
                    cantidad = sc.nextDouble();
                    System.out.println("Equivale a " + (cantidad * dolarAReal) + " reales brasileños.\n");
                    break;
                case 4:
                    System.out.print("Ingresa la cantidad en reales brasileños: ");
                    cantidad = sc.nextDouble();
                    System.out.println("Equivale a " + (cantidad / dolarAReal) + " dólares.\n");
                    break;
                case 5:
                    System.out.print("Ingresa la cantidad en dólares: ");
                    cantidad = sc.nextDouble();
                    System.out.println("Equivale a " + (cantidad * dolarAPesoCol) + " pesos colombianos.\n");
                    break;
                case 6:
                    System.out.print("Ingresa la cantidad en pesos colombianos: ");
                    cantidad = sc.nextDouble();
                    System.out.println("Equivale a " + (cantidad / dolarAPesoCol) + " dólares.\n");
                    break;
                case 7:
                    System.out.println("Gracias por usar el conversor. ¡Hasta pronto!");
                    break;
                default:
                    System.out.println("Opción no válida. Intenta nuevamente.\n");
            }

        } while (opcion != 7);

        sc.close();
    }
}
