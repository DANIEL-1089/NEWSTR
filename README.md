#include <iostream>
#include <cstdlib>
#include <ctime>
#include <wchar.h>
#include <Windows.h>
#include <algorithm>
#include <vector>
#include <string>
#include <string.h>
#include <stdlib.h>
#include <cstring>
#include <conio.h>
#include <iomanip>
#include <process.h>



using namespace std;
class String {
private:
    char* str;
public:
    String(const char* s) {
        int lenght = strlen(s);
        str = new char[lenght + 1];
        strcpy(str, s);
    }
    ~String() {
        cout << "deleting the line\n";
        delete[] str;
    }
    void display() {
        cout << str << endl;
    }
};

int main()
{
    String s1 = "if you drive more quietly , you will continue";
    cout << "s1 = ";
    s1.display();

    return 0;
}
