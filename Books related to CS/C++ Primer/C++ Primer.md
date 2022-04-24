# Part I: The Basics

## Chapter 2 Variables and Basic Types

### 2.1 Primitive Built-in Types

#### 2.1.1 Arithmetic Types

##### Categories of Arithmetic Types

Integral Type: character and boolean types

Floating-point Type: floating, double

##### Arithmetic Types

![2.1.1-1](/Users/annalee/Desktop/Various-Notes/Books related to CS/C++ Primer/2.1.1-1.png)

1. A char is the same size as a single machine byte.
2. Actually, the size of int is decided by the length of one block of CPU(int位数取决于计算机CPU的位数)

##### Signed and Unsigned Types

For char, there are three types: char, signed char, unsigned char. char uses one of signed chars and unsigned chars, it depends on the compiler.

![2.1.1-2](/Users/annalee/Desktop/Various-Notes/Books related to CS/C++ Primer/2.1.1-2.png)

1. What is the difference between long and int?

   in 16-bit system : int is 2 bytes and long is 4 bytes

   in 32-bit system : int and long are both 4 bytes

   in 64-bit system : int is 4 bytes and long is 8 bytes, long long is also 8 bytes.

2. What is the difference between float and double? 

   float is 4 bytes and double is 8 bytes.
   float: 数符(1 bit，数的正负)，尾符(0.xxxx)，指数符(1, 指数正负)，指数
   double is the double of float :)

#### 2.1.2 Type Conversions

```
   bool b = 42; //b is true 
   int i = b; //i has value 1
   i = 3.14; // i has value 3
   double pi = i; // pi has value 3.0
   unsigned char c = -1; //assuming 8-bit char, c has value 255
   signed char c2 = 256; //assuming 8-bit chars, the value of c2 is undefined
```
![2.1.2-2](/Users/annalee/Desktop/Various-Notes/Books related to CS/C++ Primer/2.1.2-2.png)
