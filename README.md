#include <iostream>
using namespace std;

int main()
{
    int sizeArray;
	cout << "n=";
	cin >> sizeArray;
	int *A = new int[sizeArray];
    for (int i=0; i < sizeArray; i++)
	{
        cin >> A[i];
	}
    for (int i=0; i < sizeArray; i++)
	{
        for (int j=sizeArray-1; j>i; j--)
        {
            if (A[j] < A[j-1])
            {
                swap (A[j], A[j-1]);
            }
        }
    }
    for (int i=0; i < sizeArray; i++)
    {
        cout << A[i] << " ";
    }
	return 0;
}
