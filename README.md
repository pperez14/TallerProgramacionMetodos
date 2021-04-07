# TallerProgramacionMetodos

import java.util.Scanner;



public static void main(String[] args){
    Scanner teclado= new Scanner(System.in);
    System.out.println("Ingrese el número:");
    int numero=teclado.nextInt();
    boolean validar=validarNumero(numero);
    if(validar==true){
        int finalBinario=convetirBinario8Bits(numero);
        System.out.println(finalBinario);
    }if(validar==false){
        System.out.println("ERROR");
    }

}

    private static int convetirBinario8Bits(int numero) {
    int residuo;
    int binario=0;
    int exp=0;
        while (numero != 0) {
            residuo = numero % 2;
            binario += residuo * Math.pow(10, exp);
            exp++;
            numero /= 2;
        }
        return binario;
    }

    private static boolean validarNumero(int numero) {
    if(numero>-1&&numero<256){
        return true;
    }else{
        return false;
    }
    }


}
