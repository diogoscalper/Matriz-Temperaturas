# Matriz-Temperaturas
"N" dias, quais dias, menor, maior, media

using System;

namespace ConsoleApp1
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Quantos dias?\t\t");
            int n = int.Parse(Console.ReadLine());
            //criar matriz
            double[,] matTemp = new double[n, 5];
            //preencher dados das colunas
            for (int i = 0; i < n; i++)
            {
                Console.Write("Qual o dia?\t\t");
                matTemp[i, 0] = double.Parse(Console.ReadLine());
                Console.Write("Qual a temp min?\t");
                matTemp[i, 1] = double.Parse(Console.ReadLine());
                Console.Write("Qual a temp max?\t");
                matTemp[i, 2] = double.Parse(Console.ReadLine());
                //diferença entre minima e maxima
                matTemp[i, 3] = matTemp[i, 2] - matTemp[i, 1];
                //media entre min e max
                matTemp[i, 4] = (matTemp[i, 1] + matTemp[i, 2]) / 2;
            }
            Console.WriteLine("\t\tIMPRIMIR TABELA");
            Console.WriteLine("DIA" + "\tMIN." + "\tMAX." + "\tDIF." + "\tMEDIA");
            for (int i = 0; i < n; i++)
            {
                Console.WriteLine(matTemp[i, 0] + "\t" + matTemp[i, 1] + "\t" + matTemp[i, 2] + "\t" + matTemp[i, 3] + "\t" + matTemp[i, 4]);
            }
            Console.WriteLine("");
            //qual a menor minima
            double menorMin = matTemp[0, 1];
            for (int i = 0; i < n; i++)
            {
                if (matTemp[i, 1] < menorMin)
                {
                    menorMin = matTemp[i, 1];
                }
            }
            Console.WriteLine("Menor minima: \t\t" + menorMin);
            //quantos dias com menor minima
            int cont1 = 0;
            for (int i = 0; i < n; i++)
            {
                if (matTemp[i, 1] == menorMin)
                {
                    cont1++;
                }
            }
            Console.WriteLine("Quantos dias menor min:\t" + cont1);
            //dias com menor minima
            Console.Write("Dias com menor minima: \t");
            for (int i = 0; i < n; i++)
            {
                if (matTemp[i, 1] == menorMin)
                {
                    Console.Write(matTemp[i, 0] + (" / "));
                }
            }
            Console.WriteLine("");
            //qual a maior minima
            double maiorMin = matTemp[0, 1];
            for (int i = 0; i < n; i++)
            {
                if (matTemp[i, 1] > maiorMin)
                {
                    maiorMin = matTemp[i, 1];
                }
            }
            Console.WriteLine("Maior minima: \t\t" + maiorMin);
            //quantos dias com menor minima
            int cont2 = 0;
            for (int i = 0; i < n; i++)
            {
                if (matTemp[i, 1] == maiorMin)
                {
                    cont2++;
                }
            }
            Console.WriteLine("Quantos dias maior min:\t" + cont2);
            //dias com maior minima
            Console.Write("Dias com maior minima: \t");
            for (int i = 0; i < n; i++)
            {
                if (matTemp[i, 1] == maiorMin)
                {
                    Console.Write(matTemp[i, 0] + (" / "));
                }
            }
            Console.WriteLine("");
            //qual a menor maxima
            double menorMax = matTemp[0, 2];
            for (int i = 0; i < n; i++)
            {
                if (matTemp[i, 2] < menorMax)
                {
                    menorMax = matTemp[i, 2];
                }
            }
            Console.WriteLine("Menor maxima: \t\t" + menorMax);
            //quantos dias com menor maxima
            int cont3 = 0;
            for (int i = 0; i < n; i++)
            {
                if (matTemp[i, 2] == menorMax)
                {
                    cont3++;
                }
            }
            Console.WriteLine("Quantos dias menor max:\t" + cont3);
            //dias com menor maxima
            Console.Write("Dias com menor maxima: \t");
            for (int i = 0; i < n; i++)
            {
                if (matTemp[i, 2] == menorMax)
                {
                    Console.Write(matTemp[i, 0] + (" / "));
                }
            }
            Console.WriteLine("");
            //qual a maior maxima
            double maiorMax = matTemp[0, 2];
            for (int i = 0; i < n; i++)
            {
                if (matTemp[i, 2] > maiorMax)
                {
                    maiorMax = matTemp[i, 2];
                }
            }
            Console.WriteLine("Maior maxima: \t\t" + maiorMax);
            //quantos dias com maior maxima
            int cont4 = 0;
            for (int i = 0; i < n; i++)
            {
                if (matTemp[i, 2] == maiorMax)
                {
                    cont4++;
                }
            }
            Console.WriteLine("Quantos dias maior max:\t" + cont4);
            //dias com menor maxima
            Console.Write("Dias com maior maxima: \t");
            for (int i = 0; i < n; i++)
            {
                if (matTemp[i, 2] == maiorMax)
                {
                    Console.Write(matTemp[i, 0] + (" / "));
                }
            }
            Console.WriteLine("");
            //soma para medias
            double somaMin = 0;
            double mediaMin;
            double somaMax = 0;
            double mediaMax;
            double somaDif = 0;
            double mediaDif;
            //ver as diferenças de minima com maxima
            for (int i = 0; i < n; i++)
            {
                Console.WriteLine("Diferença do dia " + matTemp[i, 0] + ": \t" + matTemp[i, 3]);
            }
            //qual a menor diferença
            double menorDif = matTemp[0, 3];
            for (int i = 0; i < n; i++)
            {
                if (matTemp[i, 3] < menorDif)
                {
                    menorDif = matTemp[i, 3];
                }
            }
            Console.WriteLine("Menor diferença: \t" + menorDif);
            //quantos dias com menor diferença
            int cont5 = 0;
            for (int i = 0; i < n; i++)
            {
                if (matTemp[i, 3] == menorDif)
                {
                    cont5++;
                }
            }
            Console.WriteLine("Quantos dias menor dif:\t" + cont5);
            //dias com menor diferença
            Console.Write("Dias com menor dif: \t");
            for (int i = 0; i < n; i++)
            {
                if (matTemp[i, 3] == menorDif)
                {
                    Console.Write(matTemp[i, 0] + (" / "));
                }
            }
            Console.WriteLine("");
            //qual a maior diferença
            double maiorDif = matTemp[0, 3];
            for (int i = 0; i < n; i++)
            {
                if (matTemp[i, 3] > maiorDif)
                {
                    maiorDif = matTemp[i, 3];
                }
            }
            Console.WriteLine("Maior diferença: \t" + maiorDif);
            //quantos dias com maior diferença
            int cont6 = 0;
            for (int i = 0; i < n; i++)
            {
                if (matTemp[i, 3] == maiorDif)
                {
                    cont6++;
                }
            }
            Console.WriteLine("Quantos dias maior dif:\t" + cont6);
            //dias com maior diferença
            Console.Write("Dias com maior dif: \t");
            for (int i = 0; i < n; i++)
            {
                if (matTemp[i, 3] == maiorDif)
                {
                    Console.Write(matTemp[i, 0] + (" / "));
                }
            }
            Console.WriteLine("");
            //qual a media das diferenças
            for (int i = 0; i < n; i++)
            {
                somaDif = somaDif + matTemp[i, 3];
            }
            mediaDif = somaDif / n;
            Console.WriteLine("Media das diferenças: \t" + mediaDif);
            //media do dia
            for (int i = 0; i < n; i++)
            {
                Console.WriteLine("Media do dia " + matTemp[i, 0] + ": \t" + matTemp[i, 4]);
            }
            //media geral dos dias todos
            double somaMedia = 0;
            for (int i = 0; i < n; i++)
            {
                somaMedia = somaMedia + matTemp[i, 4];
            }
            double media = somaMedia / n;
            Console.WriteLine("Media geral dos dias: \t" + media.ToString("F2"));
            //media das minimas e maximas
            for (int i = 0; i < n; i++)
            {
                somaMin = somaMin + matTemp[i, 1];
                somaMax = somaMax + matTemp[i, 2];
            }
            mediaMin = somaMin / n;
            mediaMax = somaMax / n;
            Console.WriteLine("Media das minimas: \t" + mediaMin.ToString("F2"));
            Console.WriteLine("Media das maximas: \t" + mediaMax.ToString("F2"));
        }
    }
}
