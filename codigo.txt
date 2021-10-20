#include <iostream>
#include <conio.h>
#include <windows.h>
#define limpiar system ("cls")
using namespace std;

int main()
{
    int A[50][50], B[50][50], R[50][50];
    int a = 3, m = 0, r = 0;
    cout << "Filas de A: "; cin >> a;
    cout << "Columnas de A: "; cin >> m;
    cout << endl;
    for (int i = 0; i < a; ++i)
        for (int x = 0; x < m; ++x)
        {
            cout << "Ingrese Matriz A[" << i << "][" << x << "]: ";
            cin >> A[i][x];
        }
    cout << "Filas de B: " << m << endl;
    cout << "Columnas de B: "; cin >> r;
    cout << endl;
    for (int i = 0; i < m; ++i)
        for (int x = 0; x < r; ++x)
        {
            cout << "Ingrese Matriz B[" << i << "][" << x << "]: ";
            cin >> B[i][x];
        }
    cout << endl;
    for (int i = 0; i < a; ++i)
        for (int x = 0; x < r; ++x)
            R[i][x] = 0;
    for (int i = 0; i < a; ++i)
        for (int x = 0; x < r; ++x)
            for (int z = 0; z < m; ++z)
                R[i][x] += A[i][z] * B[z][x];
    cout << "Matriz A: " << endl;
    for (int i = 0; i < a; ++i)
    {
        for (int x = 0; x < m; ++x)
        {
            cout << A[i][x] << " ";
        }
        cout << endl;
    }
    cout << "Matriz B: " << endl;
    for (int i = 0; i < m; ++i)
    {
        for (int x = 0; x < r; ++x)
        {
            cout << B[i][x] << " ";
        }
        cout << endl;
    }
    cout << "Matriz Resultante: " << endl;
    for (int i = 0; i < m; ++i)
    {
        for (int x = 0; x < r; ++x)
        {
            cout << R[i][x] << " ";
        }
        cout << endl;
    }
    return 0;
}