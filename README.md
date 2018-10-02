///Main Insercion/////

package OrdenarInsercion;

public class Main {

public static void main(String[] args) {
	int arreglo[]= {5,11,13,15,4,12,23,3,4,2,1,45,13};
	
	OrdenarInsercion o= new OrdenarInsercion();
	o.Ordenar(arreglo);
	
	for(int i=0; i<arreglo.length;i++) {
		System.out.println(arreglo[i]);
	}

}
}

////7ORDENAMIENTO INSERCION//////

package OrdenarInsercion;

public class OrdenarInsercion {

public void Ordenar(int[] array) {
	
	int aux;
	int cont1,cont2;

	for(cont1 = 1; cont1 < array.length; cont1++) {
		aux= array[cont1];
		
		for(cont2 = cont1-1; cont2>=0 && array[cont2] > aux; cont2--) {
			array[cont2+1]=array[cont2];
			array[cont2] = aux;
		}
	}
}
}

/////Main burbuja////////

package Ordenar;

public class Main {

public static void main(String[] args) {
	// TODO Auto-generated method stub
	int arreglo[] = {10, 4, 3, 9, 2, 23, 5, 4};
	
	OrdenamientoBurbuja o = new OrdenamientoBurbuja();
	o.OrdenamientoBurbuja(arreglo);
	
	for(int i = 0; i < arreglo.length; i++) {
		System.out.println(arreglo[i]);
	}
}
}

//////ORDENAMIENTO BURBUJA//////

package Ordenar;

public class OrdenamientoBurbuja {

public void OrdenamientoBurbuja(int [] array) {
	
	int aux;
	boolean cambiar = false;
	
	while(true) {
		cambiar = false;
		
		for(int i=1; i<array.length; i++) {
			if(array[i]<array[i-1]) {
				aux=array[i];
				array[i]=array[i-1];
				array[i-1]=aux;
				cambiar=true;
			}
		}
		
		if(cambiar==false)
			break;
	}
}
}
