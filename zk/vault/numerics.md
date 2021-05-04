# Numerica, ricerche varie


## Floating point stuff
- [What Every Computer Scientist Should Know About Floating-Point Arithmetic](https://docs.oracle.com/cd/E19957-01/806-3568/ncg_goldberg.html)

- [Single Precision](https://en.wikipedia.org/wiki/Single-precision_floating-point_format)
- [Float to decimal converter](https://www.h-schmidt.net/FloatConverter/IEEE754.html)
- [What's the difference between a single precision and double precision floating point operation?](https://stackoverflow.com/questions/801117/whats-the-difference-between-a-single-precision-and-double-precision-floating-p)
```
0 00000000 00000000000000000000000 = 0
1 00000000 00000000000000000000000 = -0

0 11111111 00000000000000000000000 = Infinity
1 11111111 00000000000000000000000 = -Infinity

0 11111111 00000100000000000000000 = NaN
1 11111111 00100010001001010101010 = NaN

0 10000000 00000000000000000000000 = +1 * 2**(128-127) * 1.0 = 2
0 10000001 10100000000000000000000 = +1 * 2**(129-127) * 1.101 = 6.5
1 10000001 10100000000000000000000 = -1 * 2**(129-127) * 1.101 = -6.5

0 00000001 00000000000000000000000 = +1 * 2**(1-127) * 1.0 = 2**(-126)
0 00000000 10000000000000000000000 = +1 * 2**(-126) * 0.1 = 2**(-127)
0 00000000 00000000000000000000001 = +1 * 2**(-126) *
                                     0.00000000000000000000001 =
                                     2**(-149)  (Smallest positive value)
```

- Numeric noise https://math.stackexchange.com/questions/693958/increasing-numerical-precision-does-not-converge-numerical-solution-to-the-true
- Numeric noise again https://math.stackexchange.com/questions/3235194/truncation-error-with-growing-step-size
- Nice practical example https://math.stackexchange.com/questions/1633463/step-size-in-eulers-forward-method

- Repeating sums [sucks](https://stackoverflow.com/questions/21654098/why-there-is-no-errors-while-multiplying-floating-point-numbers) because summation is [non associative](https://en.wikipedia.org/wiki/Associative_property#:~:text=In%20mathematics%2C%20addition%20and%20multiplication,sized%20values%20are%20joined%20together.) for floats 
but can be done [right](https://en.wikipedia.org/wiki/Kahan_summation_algorithm#Alternatives) anyways.

- Good paper with premise about single precision done fine af https://link.springer.com/content/pdf/10.1007/s00382-015-2809-5.pdf

- Heun's method https://en.wikipedia.org/wiki/Heun%27s_method