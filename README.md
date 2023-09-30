#include<iostream>
using namespace std;

int main() {
    int m, n, p, q;

    cout << "Enter rows of the 1st matrix: ";
    cin >> m;
    cout << "Enter columns of the 1st matrix: ";
    cin >> n;
    
    cout << "Enter rows of the 2nd matrix: ";
    cin >> p;
    cout << "Enter columns of the 2nd matrix: ";
    cin >> q;

    if (n == p) {
        int a[m][n];
        int b[p][q];

        cout << "Enter elements of the 1st matrix:\n";
        for(int i = 0; i < m; i++) {
            for(int j = 0; j < n; j++) {
                cin >> a[i][j];
            }
        }

        cout << "Enter elements of the 2nd matrix:\n";
        for(int i = 0; i < p; i++) {
            for(int j = 0; j < q; j++) {
                cin >> b[i][j];
            }
        }

        int res[m][q];
        for(int i = 0; i < m; i++) {
            for(int j = 0; j < q; j++) {
                res[i][j] = 0;
                for(int k = 0; k < p; k++) {
                    res[i][j] += a[i][k] * b[k][j];
                }
            }
        }

        cout << "Resultant matrix:\n";
        for(int i = 0; i < m; i++) {
            for(int j = 0; j < q; j++) {
                cout << res[i][j] << " ";
            }
            cout << endl;
        }
    } else {
        cout << "Matrix multiplication is not possible." << endl;
    }

    return 0;
}..

<!---
raghuvanshi093/raghuvanshi093 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
