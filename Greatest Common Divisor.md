# Greatest Common Divisor (GCD)

## Division Operation
The division opertion formula has 4 important terms, and they are: Divident, Divisor, Quotient and Remainder. The relation of these terms can be represented as: a = b * q + r.
- Divident (a): The number that is being divided.
- Divisor (b): The number by which the divident is divided.
- Quotient (q): The result of the division.
- Remainder (r): The is what left over after the division.


## GCD Definition
The greatest commom divisor (GCD) of integers a and b is the greatest positive divisor that divids both a and b without leaving a remainder. 


## Euclidean Alogrithm
The Euclidean algorithm, a Euclid variant algorithm, which efficiently solves the GCD problem with a time complexity O(logN) where N = Max(a, b). The algorithm is based on the principle that GCD(a, b) = GCD(a, a % b).

Proof:
- Let d be any arbitrary commom divisor of a and b. We can express a = m * d and b = n * d (1).
- The relation of a and b can be represented as a = q * b + r. Therefore r = a - q * b (2).
- From (1) and (2), we find that r =  m * d - q * n * d = (m - q * n) * d. Hence d is also a divisor of r.
- This implies that the commom divisors of (a,b ,r) are the same.
- Consequently GCD(a, b) = GCD(a, r)  = GCD (b, r) = GCD (b, a % b)

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
