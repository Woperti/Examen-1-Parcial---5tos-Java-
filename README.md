# Examen-1-Parcial: Java 

## Puntos a evaluar:
### 1.Analisis: 10%
### 2.Implementación(estructura del código, orden, sin errores de sintaxis): 10%
### 3.Pruebas 10%: Probar en los siguientes casos:

Disenar un programa que cuente las vocales de una cadena de texto.

Tener en cuenta los metodos para cadenas de String
```Java
   //Convertir a minusculas
   cadena.length()
   //convertir a minusculas
   cadena.toLowerCase();
```

 
```java
   public class ContarVocales {
    
    public static int contarVocales(String cadena) {
        /* Escribe aqui tu codigo */
      
    }
/* No tocar */
    public static void testContarVocales(String cadena, int resultadoEsperado) {
        int resultadoObtenido = contarVocales(cadena);
        String vocalesEncontradas = ""; 
        String vocalesEsperadas = ""; 
        int contadorVocalesEsperadas = 0;
        
        cadena = cadena.toLowerCase(); 
        for (int i = 0; i < cadena.length(); i++) {
            char c = cadena.charAt(i); 
            if (c == 'a' || c == 'e' || c == 'i' || c == 'o' || c == 'u') {
                vocalesEncontradas += c + " ";
            }
        }

        for (int i = 0; i < resultadoEsperado; i++) {
            vocalesEsperadas += "* ";
        }

        System.out.println("Cadena: \"" + cadena + "\"");
        System.out.println("Numero de vocales esperado: " + resultadoEsperado);
        System.out.println("Numero de vocales obtenido: " + resultadoObtenido);
        System.out.println("Vocales encontradas: " + vocalesEncontradas.trim());
        System.out.println("Vocales esperadas: " + vocalesEsperadas.trim());
        
        if (resultadoObtenido == resultadoEsperado) {
            System.out.println("Test passed.");
        } else {
            System.out.println("Test case not passed. Se esperaba: " + resultadoEsperado);
        }
        System.out.println(); 
    }
    
    public static void main(String[] args) {
        System.out.println("--- Ejecutando tests ---");
        testContarVocales("Hola Mundo", 4);
        testContarVocales("Ejemplo de texto", 6);
        testContarVocales("JAVA", 2);
        testContarVocales("", 0);
    }
}
```
La salida del programa debe de ser:

![Salida](./salida-imagen.png)
