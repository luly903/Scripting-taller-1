
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
