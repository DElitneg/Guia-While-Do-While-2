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
