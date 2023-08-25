# Conversión de Unidades de Longitud

Este es un programa simple para la conversión de unidades de longitud. El programa toma una longitud en centímetros y permite al usuario elegir a qué unidad convertir.

Ejemplo:
Input: Ingrese la longitud en centímetros: 109
	  Elija la unidad a la que desea convertir: pies
Output: 3.5761 pies

## Pseudocódigo

//Aplicación para convertir unidades de longitud

Algoritmo Conversión_de_unidades
	Definir Centimetros, Resultado Como Real
	Definir Opcion1 Como Caracter
	
	Escribir "Ingresa la longitud en centímetros que deseas convertir"
	Leer Centimetros
	
	Escribir "Selecciona la unidad a la que deseas convertir:"
    Escribir "a) Metros"
    Escribir "b) Yardas"
    Escribir "c) Varas"
    Escribir "d) Pulgadas"
    Escribir "e) Pies"
    Leer Opcion1
	
	Segun Opcion1 Hacer
		"A", "a":
            Resultado = Centimetros / 100
        "B", "b":
            Resultado = Centimetros * 0.0109361
        "C", "c":
            Resultado = Centimetros / 85.34
        "D", "d":
            Resultado = Centimetros * 0.393701
        "E", "e":
            Resultado = Centimetros * 0.0328084
		De Otro Modo:
            Escribir "La opción ingresada no es válida"
	Fin Segun
	
	Escribir "Su conversión es: " Resultado
	
FinAlgoritmo

## C++

//Aplicación para convertir unidades de longitud

#include <iostream>

using namespace std;

int main() {
    float Centimetros, Resultado;
    char Opcion1;
    
    cout << "Ingresa la longitud en centimetros que deseas convertir: ";
    cin >> Centimetros;
    
    cout << "Selecciona la unidad a la que deseas convertir:" << endl;
    cout << "a) Metros" << endl;
    cout << "b) Yardas" << endl;
    cout << "c) Varas" << endl;
    cout << "d) Pulgadas" << endl;
    cout << "e) Pies" << endl;
    cin >> Opcion1;
    
    switch (Opcion1) {
        case 'A':
        case 'a':
            Resultado = Centimetros / 100;
            break;
        case 'B':
        case 'b':
            Resultado = Centimetros * 0.0109361;
            break;
        case 'C':
        case 'c':
            Resultado = Centimetros / 85.34;
            break;
        case 'D':
        case 'd':
            Resultado = Centimetros * 0.393701;
            break;
        case 'E':
        case 'e':
            Resultado = Centimetros * 0.0328084;
            break;
        default:
            cout << "La opcion ingresada no es valida" << endl;
            return 1; 
    }
    
    cout << "Su conversion es: " << Resultado << endl;
    
    return 0; 
}

## Python

//Aplicación para convertir unidades de longitud

Centimetros = float(input("Ingresa la longitud en centimetros que deseas convertir: "))

Opcion1 = input("Selecciona la unidad a la que deseas convertir:\n"
                "a) Metros\n"
                "b) Yardas\n"
                "c) Varas\n"
                "d) Pulgadas\n"
                "e) Pies\n")

if Opcion1.lower() == 'a':
    Resultado = Centimetros / 100

elif Opcion1.lower() == 'b':
    Resultado = Centimetros * 0.0109361

elif Opcion1.lower() == 'c':
    Resultado = Centimetros / 85.34

elif Opcion1.lower() == 'd':
    Resultado = Centimetros * 0.393701

elif Opcion1.lower() == 'e':
    Resultado = Centimetros * 0.0328084

else:
    print("La opción ingresada no es válida")
    exit(1)

print("Su conversión es:", Resultado)
