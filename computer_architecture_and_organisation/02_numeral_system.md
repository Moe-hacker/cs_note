# Number Systems (数制)
Number systems are a way of expressing numbers in different bases. The most common number systems are:
- Decimal (十进制): Base 10, uses digits 0-9.
- Binary (二进制): Base 2, uses digits 0-1.
- Octal (八进制): Base 8, uses digits 0-7.
- Hexadecimal (十六进制): Base 16, uses digits 0-9 and letters A-F.
# Converting Between Number Systems (数制转换)
## From all bases to decimal：
To convert a number from any base to decimal, multiply each digit by its base raised to the power of its position (counting from right to left, starting at 0), and then sum the results.
For example, to convert the binary number 1001 to decimal:
| 2^3 | 2^2 | 2^1 | 2^0 |
|-----|-----|-----|-----|
|  1  |  0  |  0  |  1  |
= 1*2^3 + 0*2^2 + 0*2^1 + 1*2^0 
= 8 + 0 + 0 + 1 = 9 (decimal)
To convert the hexadecimal number 1A3 to decimal:
| 16^2 | 16^1 | 16^0 |
|------|------|------|
|  1   |  A   |  3   |
= 1*16^2 + 10*16^1 + 3*16^0 
= 256 + 160 + 3 = 419 (decimal)
## From decimal to other bases：
To convert a decimal number to another base, repeatedly divide the number by the new base and record the remainders. The remainders, read in reverse order, give the number in the new base.
For example, to convert the decimal number 45 to binary:
| 2 | 45 | 1 |
|   | 22 | 0 |
|   | 11 | 1 |
|   | 5  | 1 |
|   | 2  | 0 |
|   | 1  | 1 |
|   | 0  |   |

Reading the remainders in reverse order gives 101101 (binary).
To convert the decimal number 514 to hexadecimal:
| 16 | 514 | 2 |
|    | 32  | 0 |
|    | 2   | 2 |
|    | 0   |   |

Reading the remainders in reverse order gives 202 (hexadecimal).

Or, using table, for 45(decimal):
64 | 32 | 16 | 8 | 4 | 2 | 1
---|----|----|---|---|---|---
 0 |  1 |  0 | 1 | 1 | 0 | 1
 45 = 32 + 8 + 4 + 1 = 101101 (binary)
For 514(decimal):
256 | 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1
----|-----|----|----|----|---|---|---|---
 2  |  0  | 2  | 0  | 0  | 0 | 2 | 0 | 0
514 = 2*256 + 2*2 = 202 (hexadecimal)
I prefer the table method.