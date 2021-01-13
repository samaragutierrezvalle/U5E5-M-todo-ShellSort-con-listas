# U5E5-M-todo-ShellSort-con-listas
package shellsort;

import java.util.ArrayList;
import java.util.List;

public class shellsort {

    
    public static void main(String[] args) {
         List<Integer> lista = new ArrayList<Integer>();
       lista.add(3);
       lista.add(5);
       lista.add(24);
       lista.add(1);
       lista.add(10);
       lista.add(11);
       lista.add(4);
       lista.add(7);
       lista.add(2);
       lista.add(10);
       
         System.out.println("areglo desordenado");
         for(int j=0;j<lista.size();j++){
          System.out.print(lista.get(j)+" ");
        }
        metodoShellsort(lista);
        System.out.println("");
        System.out.println("Arreglo ordenado");
         for(int j=0;j<lista.size();j++){
          System.out.print(lista.get(j)+" ");
      }
    }

    private static void metodoShellsort( List<Integer> lista ) {
        int division = lista.size()/2, aux,salto, i;
        for(salto=division; salto!=0; salto/=2){
            boolean cambio=true;
            while(cambio){
                cambio=false;
                for(i=salto; i<lista.size(); i++){
                    if (lista.get(i-salto)>lista.get(i)){
                        aux=lista.get(i);
                        lista.set(i,lista.get(i-salto));
                        lista.set(i-salto,aux);
                        cambio=true;
                    }
                }
            }
        }
    }

    
    
}
