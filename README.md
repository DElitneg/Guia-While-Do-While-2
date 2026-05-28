# Guia-While-Do-While-2
GUÍA DE TRABAJO PRÁCTICO N° 2

// 1)
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApplication1
{
    class Program
    {
        static void Main(string[] args)
        {

            String opcion;
            int SaldoInicial;
            SaldoInicial = 10000;
            int deposito;
            deposito = 0;

            do
            {
                Console.WriteLine("Opciones: ");
                Console.WriteLine("1. Depositar dinero");
                Console.WriteLine("2. Retirar dinero");
                Console.WriteLine("3. Ver saldo actual");
                Console.WriteLine("4. [Salir]");
                Console.Write("Eleccion: ");
                opcion = Convert.ToString(Console.ReadLine());

                switch (opcion)
                {
                    case "1":
                        Console.Write("Cuanto va a depositar?: ");
                        deposito = int.Parse(Console.ReadLine());
                        SaldoInicial += deposito;
                        Console.WriteLine("A depositado " + deposito + ", su saldo es de " + SaldoInicial);
                        break;

                    case "2":
                        Console.Write("Cuanto va a retirar?: ");
                        deposito = int.Parse(Console.ReadLine());                                               
                        if (deposito > SaldoInicial)
                        {
                            Console.WriteLine("El retiro excede su saldo actual de " + SaldoInicial);
                        }                        
                        else if (deposito <= SaldoInicial)
                        {
                            SaldoInicial = SaldoInicial - deposito;
                            Console.WriteLine("Se a retirado " + deposito + ", queda " + SaldoInicial);
                        }
                        break;                    

                    case "3":
                        Console.WriteLine("Su saldo actual es de "+SaldoInicial);
                        break;

                    case "4":
                        Console.WriteLine("Saliendo del programa . . .");
                        break;

                    default:
                        Console.WriteLine("Opcion invalida");
                        break;
                }
            } while (opcion != "4");

        }
    }
}

// 2)
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApplication1
{
    class Program
    {
        static void Main(string[] args)
        {
            int numeroSecreto, contador, numero;
            numeroSecreto = 42;
            contador = 0;
            Console.WriteLine("Adivina el numero secreto ");
            do
            {
                Console.Write("Numero: ");
                numero = int.Parse(Console.ReadLine());
                if(numero<numeroSecreto)
                {
                    Console.WriteLine("El numero secreto es mayor");
                }
                else if(numero>numeroSecreto)
                {
                    Console.WriteLine("El numero secreto es menor");
                }
                contador += 1;
            } while (numero != numeroSecreto && contador < 5);

            Console.WriteLine("El numero secreto era " + numeroSecreto);

        }
    }
}

// 3)
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApplication1
{
    class Program
    {
        static void Main(string[] args)
        {

            int valor, ahorro, contador, mayor;
            String respuesta;
            ahorro = 0; contador = 0; mayor = 0;

            do
            {
                Console.Write("Ingrese el monto de la venta: ");
                valor = int.Parse(Console.ReadLine());
                Console.WriteLine("Desea continuar ingresando ventas? (Y/N):");
                respuesta = Convert.ToString(Console.ReadLine());
                if(valor>mayor)
                {
                    mayor = valor;
                }
                contador += 1;
                ahorro += valor;
            } while (respuesta == "Y");
            Console.WriteLine("El total acumulado es: " + ahorro+", hubo "+contador+" ventas, y la mayor fue de "+mayor);

        }
    }
}

// 4)
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApplication1
{
    class Program
    {
        static void Main(string[] args)
        {
            
            int contador; contador = 0;
            String usuario, contraseña;
            String contraseñareal, usuarioreal;
            contraseñareal = "contraseña";
            usuarioreal = "usuario";
            do
            {
                Console.Write("Ingrese nombre de Usuario: ");
                usuario = Convert.ToString(Console.ReadLine());
                Console.Write("Ingrese contraseña: ");
                contraseña = Convert.ToString(Console.ReadLine());
                contador += 1;
                if(contraseña == contraseñareal && usuario == usuarioreal)
                {
                    contador = 3;
                    Console.WriteLine("Bienvenido al sistema");
                }
                else if(contraseña != contraseñareal || usuario != usuarioreal)
                {
                    Console.WriteLine("Usuario o contraseña incorrecto");
                }
            } while (contador != 3);
            if (contador == 3 && contraseña != contraseñareal)
            {
                Console.WriteLine("Cuenta bloqueada por seguridad");
            }
        }
    }
}

// 5)
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApplication1
{
    class Program
    {
        static void Main(string[] args)
        {
            
            int numero, contador, negativos, positivos, ceros;
            contador = 0; negativos = 0; ceros = 0; positivos = 0;
            String respuesta;


            Console.WriteLine("Ingrese numeros positivos, negativos o ceros, el programa se detendra al introducir X");

            do
            {
                Console.Write("Numero: ");
                numero = int.Parse(Console.ReadLine());
                Console.Write("Continuar?: ");
                respuesta = Convert.ToString(Console.ReadLine());

                contador += 1;

                if(numero > 0)
                {
                    positivos += 1;
                }
                else if(numero<0)
                {
                    negativos += 1;
                }
                else if(numero == 0)
                {
                    ceros += 1;
                }
  
            } while (respuesta != "X");

            Console.WriteLine("Positivos: " + positivos +" Negativos: "+negativos+" Ceros: "+ceros);
                
        }
    }
}
REVERIFICAR EL 5

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApplication1
{
    class Program
    {
        static void Main(string[] args)
        {

            int numero, contador, negativos, positivos, ceros;
            contador = 0; negativos = 0; ceros = 0; positivos = 0;
            String respuesta;


            Console.WriteLine("Ingrese numeros positivos, negativos o ceros, el programa se detendra al introducir X");

            do
            {
                Console.Write("Numero: ");
                numero = int.Parse(Console.ReadLine());

                contador += 1;

                if (numero > 0)
                {
                    positivos += 1;
                }
                else if (numero < 0)
                {
                    negativos += 1;
                }
                else if (numero == 0)
                {
                    ceros += 1;
                }

                respuesta = numero.ToString();

            } while (respuesta != "X");

            Console.WriteLine("Positivos: " + positivos + " Negativos: " + negativos + " Ceros: " + ceros);

        }
    }
}
el 5 no funciona
