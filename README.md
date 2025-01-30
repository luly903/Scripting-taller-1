# Scripting-taller-1
miembros del equipo: 
- Juliana Monroy Andrade
- Paulina Serna Alzate
- Manuela Barrera Neira

## Ejercicios:

Ejercicio #1:
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

# Firmas:
