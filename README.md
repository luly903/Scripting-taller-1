# Scripting-taller-1
miembros del equipo: 
- Juliana Monroy Andrade
- Paulina Serna Alzate
- Manuela Barrera Neira

## Ejercicios:

Ejercicio #1:
```
namespace ejercicio_1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            int[,] matriz1 = new int[3,3];
            int[,] matriz2 = new int[3,3];
            Random numero = new Random();
            for (int i=0; i <3;i++)
            {
                for (int j = 0; j < 3; j++)
                {
                    matriz1[i,j] = numero.Next(-50,51);
                }
            }
            for (int i = 0; i < 3; i++)
            {
                for (int j = 0; j < 3; j++)
                {
                    if (matriz1[i, j] < 0)
                    {
                        matriz2[i, j] = matriz1[i, j] * -1;
                    }
                    else 
                    {
                        matriz2[i, j] = matriz1[i, j];
                    }
                }
            }
            Console.WriteLine("La matriz original es:");
            for (int i = 0; i < 3; i++)
            {
                for (int j = 0; j < 3; j++)
                {
                    Console.Write(matriz1[i, j]+" | ");
                }
                Console.WriteLine();
            }
            Console.WriteLine("La matriz positiva es:");
            for (int i = 0; i < 3; i++)
            {
                for (int j = 0; j < 3; j++)
                {
                    Console.Write(matriz2[i, j] + " | ");
                }
                Console.WriteLine();
            }
        }
    }
}
```
Ejercicio #7:
```
namespace ejercicio_7
{
    internal class Program
    {
        static void Main(string[] args)
        {
            string cadena ="" ;
            string[] array = new string[30];
            Console.WriteLine("Escriba la cadena dejando un espacio entre cada numero:");
            cadena=Console.ReadLine();
            array=cadena.Split();
            for(int i = 0; i < array.Length; i++) 
            {
Console.Write(array[i]+" | ");
            }
        }
    }
}
```
Ejercicio #15:
```
using System;
using System.Linq; 

namespace ejercicio_18
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Ingrese la cadena dejando un espacio entre cada letra:");
            string cadena = Console.ReadLine();

           
            string[] ca = cadena.Split(' ');
            string[] cad = new string[ca.Length];

            
            for (int i = 0; i < ca.Length; i++)
            {
                cad[i] = ca[ca.Length - 1 - i];
            }

           
            if (ca.SequenceEqual(cad))
            {
                Console.WriteLine("Esta cadena es palíndroma.");
            }
            else
            {
                Console.WriteLine("Esta cadena no es palíndroma.");
            }
        }
    }
}
```
Ejercicio #18:
```
using System;
class Program
{
    static void Main()
    {
        string num;

        Console.WriteLine("ingrese un numero de 1 a 8 digitos");
        num = Console.ReadLine();

        if(num.Length <= 0 || num.Length > 8)
        {
            Console.WriteLine("numero invalido, escriba un numero de 1 a 8 digitos");
            num = Console.ReadLine();

        }

        int resultado = Suma(num);
        Console.WriteLine("el resultado de la suma de los digitos es: "+resultado);   
 

    }

    public static int Suma(string num)
    {
  
        int sumaTotal = 0;
        int numero = int.Parse(num);    
      
            while (numero >= 10)
            {
                int suma = 0;
                while (numero > 0)
                {
                    suma += numero % 10;  // el simbolo % Extrae el último dígito y lo suma
                    numero /= 10;        
                }
                numero = suma; 
            }

        

        return numero;
    }
```
Ejercicio #26:
```
using System;
using System.Transactions;
class Program
{
    static void Main()
    {
        int cont = 0;
        float num = 0;
        string rpta = "";
        double acum = 0;
        double prom =0;

        Console.WriteLine("ingrese un numero flotante, cuando desee saber el promedio de los numeros ingresados, digite ´x´");

        while (rpta != "x")
        {
            Console.WriteLine("ingrese un numero o ´x´");
            rpta = Console.ReadLine();

            if (rpta != "x")
            {
                cont++;

                try
                {
                    num = float.Parse(rpta);
                }
                catch
                {
                    Console.WriteLine("invalido: escribiste una letra o palabra que no fuera ´x´, por favor ingresa un numer o la letra ´x´ ");
                }
                

                acum = acum + num;

                prom = acum / cont;
            
                Console.WriteLine("ingrese otro numero o ´x´ para conocer el promedio final");

            }


        }

        Console.WriteLine("el promedio de los numeros es: " + prom);
    }


}
```
# Firmas:
1:
```
public static bool EsNegativo(int num)
{
    return num < 0;
}
```
Invocación: 
```
bool respuesta = EsNegativo(9);
```
2: 
```
public static void Saludo()
{
    Console.WriteLine("¡hello world!");
}
```
invocación: 
```
saludo();
```
3:
```
public static int Suma(int a, int b)
{
 return a + b;
}
```
Invocación: 
```
Sumar(5, 7);
```
4:
```
public static void menu()
{

    Console.Writeline("-------------------MENU-------------------");
    Console.Writeline("1. pollo asado      2. carne a la parrilla");
    Console.Writeline("3. ensalada cesar   4. menu infantil ");

}
```
Invocación: 
```
menu();
```
5:
```
public static bool EsPositivo(int num)
{
    return num > 0;
}
```
Invocación: 
```
bool respuesta = EsPositivo(5);
```
6:
```
public string SaludarPersona(string nombre)
{
    return "¡Hola, " + nombre + "!";
}
```
Invocación:
```
Console.WriteLine(SaludarPersona("Carlos"));
```
7:
```
static int Multiplicar(int x, int y)
{
    return x * y;
}
```
Invocación:
```
Console.WriteLine("El producto es: " + Multiplicar(3, 4));
```
8:
```
static int Mayor(int a, int b)
{
    return a > b ? a : b;
}
```
Invocación:
```
Console.WriteLine("El número mayor es: " + Mayor(12, 8));
```
9:
```
static void MostrarNumeros(int[] numeros)
{
    foreach (int num in numeros)
    {
        Console.WriteLine(num);
    }
}
```
Invocación:
```
int[] numeros = {1, 2, 3, 4, 5};
MostrarNumeros(numeros);
```
10:
```
public int ContarCaracteres(string cadena)
{
    return cadena.Length;
}
```
Invocación:
```
Console.WriteLine("La cadena tiene " + ContarCaracteres("Programación") + " caracteres.");
```
11:
```
static double CalcularAreaRectangulo(double baseRect, double altura)
{
    return baseRect * altura;
}
```
Invocación:
```
Console.WriteLine("El área es: " + CalcularAreaRectangulo(5, 10));
```
12:
```
static bool EsPalindromo(string palabra)
{
    string invertida = new string(palabra.Reverse().ToArray());
    return palabra == invertida;
}
```
Invocación:
```
Console.WriteLine(EsPalindromo("oso") ? "Es palíndromo" : "No es palíndromo");
```
13:
```
public int EncontrarMayor(int[] numeros)
{
    return numeros.Max();
}
```
Invocación:
```
int[] lista = { 3, 7, 2, 9, 5 };
Console.WriteLine("El número mayor es: " + EncontrarMayor(lista));
```
14:
```
static double ConvertirFahrenheit(double celsius)
{
    return (celsius * 9/5) + 32;
}
```
Invocación:
```
Console.WriteLine("Temperatura en Fahrenheit: " + ConvertirFahrenheit(25));
```
15:
```
static List<int> NumerosPares(int n)
{
    return Enumerable.Range(1, n).Where(i => i % 2 == 0).ToList();
}
```
Invocación:
```
Console.WriteLine(string.Join(", ", NumerosPares(10)));
```
16:
```
public string ObtenerFechaHora()
{
    return DateTime.Now.ToString();
}

```
Invocación:
```
onsole.WriteLine("Fecha y hora: " + ObtenerFechaHora());
```
17:
```
static string InvertirCadena(string texto)
{
    return new string(texto.Reverse().ToArray());
}
```
Invocación:
```
Console.WriteLine("Invertida: " + InvertirCadena("programación"));
```
18:
```
public int SumarArray(int[] numeros)
{
    return numeros.Sum();
}
```
Invocación:
```
int[] valores = { 4, 7, 1, 9 };
Console.WriteLine("Suma total: " + SumarArray(valores));
```
19:
```
public void UnirNombres(string[] nombres)
{
    Console.WriteLine("Nombres: " + string.Join(" | ", nombres));
}
```
Invocación:
```
UnirNombres(new string[] { "Ana", "Carlos", "Elena" });
```
20:
```
static void FormatearNumeros(int[] numeros, string separador)
{
    Console.WriteLine("Lista formateada: " + string.Join(separador, numeros));
}
```
Invocación:
```
FormatearNumeros(new int[] { 1, 2, 3, 4, 5 }, " - ");
```
