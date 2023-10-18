# CPP-Basic_RoadMapByRM : Chapter-1 Basic Operations

## Arithmetic Operators in C++

### Addition (+)
```cpp
int a = 5, b = 10;
int sum = a + b;  // sum will be 15
```

### Subtraction (-)
```cpp
int a = 15, b = 10;
int difference = a - b;  // difference will be 5
```

### Multiplication (*)
```cpp
int a = 5, b = 4;
int product = a * b;  // product will be 20
```

### Division (/)
```cpp
int a = 20, b = 4;
int quotient = a / b;  // quotient will be 5

double c = 22.0, d = 7.0;
double result = c / d;  // result will be an approximation of 3.142857
```

### Modulus (%)
```cpp
int a = 10, b = 3;
int remainder = a % b;  // remainder will be 1
```

### Increment (++)
```cpp
int a = 5;
a++;  // a will be 6
```

### Decrement (--)
```cpp
int a = 5;
a--;  // a will be 4
```

## Logical Operators in C++

### Logical AND (&&)
```cpp
bool a = true, b = false;
bool result = a && b;  // result will be false
```

### Logical OR (||)
```cpp
bool a = true, b = false;
bool result = a || b;  // result will be true
```

### Logical NOT (!)
```cpp
bool a = true;
bool result = !a;  // result will be false
```

Let's take a look at a practical example where these operators might be used:

```cpp
std::string username = "user123";
std::string password = "pass123";

bool isUsernameValid = (username == "user123");
bool isPasswordValid = (password == "pass123");

if (isUsernameValid && isPasswordValid) {
    std::cout << "Logged in successfully!" << std::endl;
} else {
    std::cout << "Invalid credentials!" << std::endl;
}
```

## Loops in C++

### For Loop
```cpp
for (int i = 0; i < 5; i++) {
    std::cout << i << std::endl;
}
// Output:
// 0
// 1
// 2
// 3
// 4
```

### While Loop:
```cpp
int i = 0;
while (i < 5) {
    std::cout << i << std::endl;
    i++;
}
// Output is the same as the for loop above.
```

### Do-While Loop
```cpp
int i = 0;
do {
    std::cout << i << std::endl;
    i++;
} while (i < 5);
// Output is the same as the above loops.
```

### Nested Loops
```cpp
for (int i = 0; i < 3; i++) {
    for (int j = 0; j < 3; j++) {
        std::cout << "[" << i << "][" << j << "] ";
    }
    std::cout << std::endl;
}
// Output:
// [0][0] [0][1] [0][2] 
// [1][0] [1][1] [1][2] 
// [2][0] [2][1] [2][2]
```

### Infinite Loops
```cpp
while (true) {
    // This loop will run indefinitely.
}
```

Or
```cpp
for (;;) {
    // This is also an infinite loop.
}
```

## Bitwise Operations

### Bitwise AND (&)
```cpp
int a = 5;  // Binary: 0101
int b = 3;  // Binary: 0011
int result = a & b;  // Result: 0001, which is 1 in decimal
```

### Bitwise OR (|)
```cpp
int a = 5;  // Binary: 0101
int b = 3;  // Binary: 0011
int result = a | b;  // Result: 0111, which is 7 in decimal
```

### Bitwise XOR (^)
```cpp
int a = 5;  // Binary: 0101
int b = 3;  // Binary: 0011
int result = a ^ b;  // Result: 0110, which is 6 in decimal
```

### Bitwise NOT (~)
```cpp
int a = 5;  // Binary: 0101
int result = ~a;  // Result will invert every bit: 1010
// Note: Due to how two's complement works, the value might be interpreted differently.
```

### Left Shift (<<)
```cpp
int a = 5;  // Binary: 0101
int result = a << 1;  // Result: 1010, which is 10 in decimal
```

### Right Shift (>>)
```cpp
int a = 5;  // Binary: 0101
int result = a >> 1;  // Result: 0010, which is 2 in decimal
```

Example
```cpp
int number = 5;        // Binary: 0101
int mask = 1 << 2;     // Binary: 0100
bool isBitSet = (number & mask) != 0;

if (isBitSet) {
    std::cout << "The 3rd bit is set!" << std::endl;
} else {
    std::cout << "The 3rd bit is not set!" << std::endl;
}
```

---