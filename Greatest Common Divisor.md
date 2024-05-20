# Greatest Common Divisor (GCD)

## Definitions
- Divident (a): The number that is being divided.
- Divisor (b): The number by which the divident is divided.
- Quotient (q): The result of the division.
- Remainder (r): The is what left over after the division.

The relation of these terms can be defined as: a = b * q + r

## GCD Definition
The greatest commom divisor (GCD) of integers a and b is the greatest divisor that divids both a and b without leaving a remainder. 

## Euclidean Alogrithm
The Euclidean aloghrms is an effcient algorithm of solving the GCD problem, and its time complexity is O(logN) where N = Max(a, b). The algorithm is based on the priciple that GCD(a, b) = GCD(a, a % b).

Proof:
- Let d be any arbitrary commom divisor of a and b, thus we can express a = m * d and b = n * d (1)
- The relation of a and b can be represented as a = q * b + r. Therefore r = a - k * b (2)
- From (1) and (2), r =  m * d - q * n * d = (m - q * n) * d. Hence d is also a divisor of r.
- This implies that the commom divisors of (a,b) and (b,r) are the same.
- Consequently GCD(a, b) = GCD(a, r) = GCD (a, a % b)

## Eucliden Alogorithm Implementation
```C#
       public int GCD(int a, int b)
        {
            if (b == 0)
                return a;
            else
                return GCD(b, a % b);
        }
```
