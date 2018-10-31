# description: 
 If the first operand to the logical AND operator evaluates to false the second operand is guaranteed not to evaluate.  Note: the logical OR operator is guaranteed not to evaluate the second operand if the first operand is true. Note: for the logical AND and OR operators, all side effects of the first expression, except for destruction of temporaries, happen before the second expression is evaluated.

```C++ runnable
#include <iostream>

int main(int argc, char** argv)
{
  int x = 0;
  int y = 0;

  if (x++ && y++)
  {
    y += 2;
  }

  std::cout << x + y << std::endl;

  return 0;
}
