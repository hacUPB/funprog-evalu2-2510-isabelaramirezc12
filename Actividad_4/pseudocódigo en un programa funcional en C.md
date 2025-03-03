## Introducción
¿Por qué crees que el pseudocódigo es útil antes de escribir un programa en C?

-Respuesta: El pseudocódigo es muy importante interiorizarlo e implementarlo antes de aprender a escribir en programas como C, pues le permite a los estudiantes tener una idea previa de lo que van a realizar a futuro al momento de aprender a programar en determinado lenguaje, además de que al momento de aprender terminologías y maneras específicas para programar los estudiantes pueden asociar estos términos nuevos con los ya empleados en el pseudocódigo con anterioridad.

## Estructura básica del pseudocódigo

Ejercicio:
Toma un pseudocódigo de un ejercicio anterior o escribe tu propio pseudocódigo, similar al mostrado en el ejemplo de arriba.

    INICIO

    Escribir "Ingresa un número" (x)
    Leer x
    Escribir "Ingresa otro número" (y)
    Leer y
    suma = y + x
    Escribir "Al sumar estos dos números se obtiene como resultado el número " suma

    FIN

## Traduciendo el pseudocódigo a C

¿Por qué es importante declarar el tipo de variable (int, float, etc.) antes de usarla en C?

-Respuesta: Declarar el tipo de variable en C es importante porque le permite al programa usar la memoria correctamente, evitar errores y realizar cálculos de manera precisa indicando el tipo de cada variable. Además, hace que el código sea más claro y fácil de entender.

int: números enteros.

float: números con decimales de menor precisión.

double: números con decimales de mayor precisión.

## Buenas prácticas

¿Por qué es importante comentar el código, aunque sea breve y conciso?

-Respuesta: Para dar un descripción/explicación breve que permite una mejor comprensión de lo que se ejecuta en los códigos más importantes.

## Reto final

## Reto 1

    #include <stdio.h>

    int main() {

        double X1, P1, X2, P2;
        double X, P, X2_Cuadrado, P2_Cuadrado, Dp;

        // Se piden las coordenadas

        printf("Escribir las coordenadas de X1");
        scanf("%lf", &X1);

        printf("Escribir las coordenadas de P1");
        scanf("%lf", &P1);

        printf("Escribir las coordenadas de X2");
        scanf("%lf", &X2);

        printf("Escribir las coordenadas de P2");
        scanf("%lf", &P2);

        // Cálculos
        X = X2 - X1;
        P = P2 - P1;

        X2_Cuadrado = X * X;
        P2_Cuadrado = P * P;

        Dp = sqrt(X2_Cuadrado + P2_Cuadrado); // Fórmula clave 

        // Imprimir el resultado
        printf("Distancia puntos %.2lf\n", Dp);

         return 0;
    }

## Ejercicio 2

    #include <stdio.h>

    int main() {

        double C, P;

        // Solicitar la cantidad de tela en metros
    
        printf("Ingrese la cantidad de tela que desea encargar en unidad de medida metros ");
        scanf("%lf", &C);

        // Conversión a pulgadas
        P = C / 0.0254;

        // Mostrar el resultado
        printf("La cantidad de tela que debe encargar en unidad de medida pulgadas sería %.2lf\n", P);

        return 0;
    }


## Ejercicio 3

    #include <stdio.h>

    int main() {
    
        double A, B, H;

        // Solicitar el primer cateto al usuario

        printf("Ingrese el primer valor de uno de los catetos de su triángulo ");
        scanf("%lf", &A);

        // Solicitar el segundo cateto al usuario

        printf("Ingrese el segundo valor del otro cateto de su triángulo ");
        scanf("%lf", &B);

        // Calcular la hipotenusa usando el Teorema de Pitágoras
        H = sqrt((A * A) + (B * B));

        // Mostrar el resultado

        printf("El valor de su hipotenusa es %.2lf\n", H);

        return 0;

    }

## Ejercicio 4

    #include <stdio.h>

    int main() {

        // Día, mes y año de nacimiento
        int D1, M1, A1;

        // Día, mes y año actual
        int D2, M2, A2; 

        // Edad
        int edad;

        // Solicitar la fecha de nacimiento

        printf("Ingrese su día de nacimiento ");
        scanf("%d", &D1);
    
        printf("Ingrese su mes de nacimiento ");
        scanf("%d", &M1);
    
        printf("Ingrese su año de nacimiento ");
        scanf("%d", &A1);

        // Solicitar la fecha actual

        printf("Ingrese qué día es hoy ");
        scanf("%d", &D2);
    
        printf("Ingrese qué mes es hoy ");
        scanf("%d", &M2);
    
        printf("Ingrese qué año es hoy ");
        scanf("%d", &A2);

        // Calcular la edad
        if (D1 == D2 && M1 == M2) {
            printf("¡Feliz Cumpleaños!\n");
            edad = A2 - A1;
        } 
        else if (M1 < M2 || (M1 == M2 && D1 < D2)) {
            edad = A2 - A1;
        } 
        else {
            edad = A2 - A1 - 1;
        }

        // Mostrar la edad

        printf("Tu edad es %d\n", edad);

        return 0;

     }

## Ejercicio 5

    #include <stdio.h>

    int main() {

        // Número de horas trabajadas

        int H; 

        // Pago por hora y sueldo semanal

        double P, S; 


        // Solicitar el número de horas trabajadas

        printf("Ingrese el número de horas trabajadas en la semana ");
        scanf("%d", &H);

        // Solicitar el pago por hora trabajada

        printf("Ingrese el pago que recibe por trabajar una hora ");
        scanf("%lf", &P);

        // Validar si el número de horas es mayor a 50
        if (H > 50) {
            printf("No se pueden trabajar más de 50 horas semanales\n");
            S = 0;
        } 
        else {
            if (H <= 40) {
                S = H * P;  // Pago normal
            } 
            else if (H <= 45) {
                S = (40 * P) + ((H - 40) * P * 2);  // Pago con horas extras dobles (hasta 45 horas)
            } 
            else {
                S = (40 * P) + (5 * P * 2) + ((H - 45) * P * 3); // Pago con horas extras triples (más de 45 horas)
            }
        }

        // Mostrar el sueldo semanal
        printf("El sueldo semanal es %.2lf\n", S);

        return 0;
    }

## Pregunta final

Después de este tutorial, ¿qué puntos crees que deberías reforzar para sentirte más seguro al traducir pseudocódigo a C?

-Respuesta: Repasar más el siginificado de cada concepto concretamente y hacer pequeños ejercicios de práctica como cuando se comenzó a trabajar con git bash.
