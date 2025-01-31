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
