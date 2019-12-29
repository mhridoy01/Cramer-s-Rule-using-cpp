# Cramer-s-Rule-using-cpp

#include<iostream>
using namespace std;
int main()
{
    double n;
    cout << "How many variables?   ";
    cin >> n;
    cout << endl;
    if(n == 2)
    {
        double arr[2][3];

        cout << "Enter the co-efficient:\n\n";

        for(int i = 0; i <= 1; i++)
        {
            for(int j = 0; j <= 2; j++)
            {
                cin >> arr[i][j];
            }
        }

        double D = arr[0][0] * arr[1][1] - arr[1][0] * arr[0][1];

        if(D == 0)
        {
            cout << "The equations cannot be solved\n";
        }
        else
        {
            double Dx = arr[1][1] * arr[0][2] - arr[0][1] * arr[1][2];
            double Dy = arr[1][2] * arr[0][0] - arr[0][2] * arr[1][0];
            double x = Dx / D;
            double y = Dy / D;

            cout << endl;
            cout << "x = " << x << "  " << "y = " << " " << y;
        }
    }

    else if(n == 3)
    {
        double arr[3][4];

        cout << "Enter the co-efficient:\n\n";

        for(int i = 0; i <= 2; i++)
        {
            for(int j = 0; j <= 3; j++)
            {
                cin >> arr[i][j];
            }
        }

        double D = arr[0][0] * (arr[1][1] * arr[2][2] - arr[2][1] * arr[1][2]) - arr[0][1] * (arr[1][0] * arr[2][2] - arr[2][0] * arr[1][2]) + arr[0][2] * (arr[1][0] * arr[2][1] - arr[2][0] * arr[1][1]);

        if(D == 0)
        {
            cout << "The equations cannot be solved\n";
        }
        else
        {
            double Dx = arr[0][3] * (arr[1][1] * arr[2][2] - arr[2][1] * arr[1][2]) - arr[0][1] * (arr[1][3] * arr[2][2] - arr[2][3] * arr[1][2]) + arr[0][2] * (arr[1][3] * arr[2][1] - arr[2][3] * arr[1][1]);
            double Dy = arr[0][0] * (arr[1][3] * arr[2][2] - arr[2][3] * arr[1][2]) - arr[0][3] * (arr[1][0] * arr[2][2] - arr[2][0] * arr[1][2]) + arr[0][2] * (arr[1][0] * arr[2][3] - arr[2][0] * arr[1][3]);
            double Dz = arr[0][0] * (arr[1][1] * arr[2][3] - arr[2][1] * arr[1][3]) - arr[0][1] * (arr[1][0] * arr[2][3] - arr[2][0] * arr[1][3]) + arr[0][3] * (arr[1][0] * arr[2][1] - arr[2][0] * arr[1][1]);
            double x = Dx / D;
            double y = Dy / D;
            double z = Dz / D;

            cout << endl;
            cout << "x = " << " " << x << "  " << "y = " << "  " << y << "  " <<"z = " << "  " << z;
        }
    }
}
