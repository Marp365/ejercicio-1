Diseña un programa que lea las calificaciones de 30 estudiantes, las almacene en un arreglo y calcule el promedio general. Además, muestra cuántos estudiantes están por encima del promedio.

#include <iostream>
using namespace std;

int main() {
    float calificaciones[30], suma = 0, promedio;
    int contador = 0;

    for (int i = 0; i < 30; i++) {
        cout << "Ingrese la calificación del estudiante " << i + 1 << ": ";
        cin >> calificaciones[i];
        suma += calificaciones[i];
    }

    promedio = suma / 30;

    for (int i = 0; i < 30; i++) {
        if (calificaciones[i] > promedio) {
            contador++;
        }
    }

    cout << "Promedio general: " << promedio << endl;
    cout << "Estudiantes por encima del promedio: " << contador << endl;

    return 0;
}


