//6.Выполнить задание, оформив его через функции (ввода, вывода, заполнение). 
//Передачу массива в функции организовать через указатели.
//Получить квадратную матрицу порядка n, элементами которой являются заданные 
//числа а1, …, аnn, расположенные в ней по спирали(см.схему на рисунке).
//Перебор строк / столбцов матрицы осуществить с использованием указателей.

/*
4
10  9  8  7
11 16 15  6
12 13 14  5
 1  2  3  4

5
13 12 11 10  9
14 23 22 21  8
15 24 25 20  7
16 17 18 19  6
 1  2  3  4  5
*/

#include <iostream>
#include <iomanip>
using namespace std;

void Input(int& n);
void Fill(int* matrix, int n);
void Output(int* matrix, int n);

int main()
{
    int matrix[1000];
    int n;
    cout << "enter matrix size: ";
    Input(n);
    Fill(matrix, n);
    Output(matrix, n);
    return 0;
}

void Input(int &n)
{
    cin >> n;
}

void Fill(int *matrix, int n)
{
    int x = n / 2, y = n / 2;
    int sign = 1;
    int value = n * n;
    if (n % 2 == 0)
    {
        x--;
        y--;
        sign *= -1;
    }
    *(matrix + y * n + x) = value;
    for (int i = 1; i < n; i++)
    {
        sign *= -1;
        for(int j = 0; j < i; j++)
        {
            value--;
            x += sign;
            *(matrix + y * n + x) = value;
        }
        for (int j = 0; j < i; j++)
        {
            value--;
            y += sign;
            *(matrix + y * n + x) = value;
        }
    }
    for (int i = 0; i < n - 1; i++)
        *(matrix + (n-1)*n + i) = i+1;
}

void Output(int *matrix, int n)
{
    for (int i = 0; i < n; i++)
    {
        for (int j = 0; j < n; j++)
            cout << setw(3) << *(matrix + i * n + j);
        cout << '\n';
    }
}


