
#SourceCode Upload test
## test1

```
#include <iostream>
using namespace std;

void make_square(int width, int length)
{
    for (int i = 0; i < length; i++) {
        for (int idx = 0; idx < width; idx++) {
            cout << "■";
        }
        cout << endl;
    }
}

int main()
{
    make_square(5, 5);
}
```
