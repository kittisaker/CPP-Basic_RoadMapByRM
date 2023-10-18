# CPP-Basic_RoadMapByRM : Chapter-2 Functions

## Functions in C++
```cpp
#include <iostream>

// Function prototype
int add(int, int); 

int main() {
    int result = add(5, 7);
    std::cout << "The sum is: " << result << std::endl;
    return 0;
}

// Function definition
int add(int a, int b) {
    return a + b;
}
```

## Lambda Functions in C++
The general syntax for lambda functions is:
```cpp
[capture](parameters) -> return_type { body_of_lambda }
```
- capture: This captures external variables for use inside the lambda.
- parameters: Like regular functions, you can pass arguments to lambdas.
- return_type: This is optional and if skipped, it's inferred from the return statements in the lambda.
- body_of_lambda: The code that the lambda will execute.

### 1. A Simple Lambda
```cpp
auto simpleLambda = []() {
    std::cout << "Hello from Lambda!" << std::endl;
};

simpleLambda();  // Outputs: Hello from Lambda!
```

### 2. Lambda with Parameters
```cpp
auto add = [](int a, int b) {
    return a + b;
};

std::cout << add(3, 4);  // Outputs: 7
```

### 3. Lambda with Explicit Return Type
```cpp
auto divide = [](double a, double b) -> double {
    if (b == 0.0) {
        return 0.0;  // Handle division by zero
    }
    return a / b;
};

std::cout << divide(5.0, 2.0);  // Outputs: 2.5
```

### 4. Lambda with Captures
```cpp
int x = 10;
int y = 20;

auto addXY = [x, y]() {
    return x + y;
};

std::cout << addXY();  // Outputs: 30
```

There are other ways to capture, such as:
[=]: Capture all local variables by value.
[&]: Capture all local variables by reference.
[x, &y]: Capture x by value and y by reference.

### 5. Lambdas as Function Arguments
```cpp
std::vector<int> numbers = {5, 2, 8, 1, 3};

std::sort(numbers.begin(), numbers.end(), [](int a, int b) {
    return a > b;
});

for (int n : numbers) {
    std::cout << n << " ";  // Outputs: 8 5 3 2 1
}
```

---