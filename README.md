# Euclidean-Algorithm
The code provided calculates the **greatest common divisor** (GCD) of two integers, N1 and N2, with N1>N2. 

When the two numbers N1 and N2 are coprime, i.e., their GCD is 1, the code calculates the **modular multiplicative inverse** of N2 module N1, i.e., it calculates the integer N such that 

N2 * N $\equiv$ 1 (mod N1). 


## Example 1
 N1 = 59, N2 = 19
```
( 1 )	 59 = 0 (mod 59 )
( 2 )	 19 =  19  (mod 59 )
		 2 =  59 - 3 * 19  (mod N1)
( 3 )	 2 =  -3 * 19  (mod N1)
		 1 =  19 - 9 * 2  (mod N1)
( 4 )	 1 =  28 * 19  (mod N1)

The inverse multiplicative of 19 (mod 59) is 28
i.e., 19 * 28 = 1 (mod 59)
```
## Example 2
 N1 = 123456789, N2 = 5432
```
( 1 )	 123456789 = 0 (mod 123456789 )
( 2 )	 5432 =  5432  (mod 123456789 )
		 3725 =  123456789 - 22727 * 5432  (mod N1)
( 3 )	 3725 =  -22727 * 5432  (mod N1)
		 1707 =  5432 - 1 * 3725  (mod N1)
( 4 )	 1707 =  22728 * 5432  (mod N1)
		 311 =  3725 - 2 * 1707  (mod N1)
( 5 )	 311 =  -68183 * 5432  (mod N1)
		 152 =  1707 - 5 * 311  (mod N1)
( 6 )	 152 =  363643 * 5432  (mod N1)
		 7 =  311 - 2 * 152  (mod N1)
( 7 )	 7 =  -795469 * 5432  (mod N1)
		 5 =  152 - 21 * 7  (mod N1)
( 8 )	 5 =  17068492 * 5432  (mod N1)
		 2 =  7 - 1 * 5  (mod N1)
( 9 )	 2 =  -17863961 * 5432  (mod N1)
		 1 =  5 - 2 * 2  (mod N1)
( 10 )	 1 =  52796414 * 5432  (mod N1)

The inverse multiplicative of 5432 (mod 123456789) is 52796414
i.e., 5432 * 52796414 = 1 (mod 123456789)
```
## Example 3
N1 = 48, N2 = 18
```
( 1 )	 48 = 0 (mod 48 )
( 2 )	 18 =  18  (mod 48 )
		 12 =  48 - 2 * 18  (mod N1)
( 3 )	 12 =  -2 * 18  (mod N1)
		 6 =  18 - 1 * 12  (mod N1)
( 4 )	 6 =  3 * 18  (mod N1)
		 0 =  12 - 2 * 6  (mod N1)
( 5 )	 0 =  -8 * 18  (mod N1)

The greatest common divisor (GCD) of  48  and  18  is  6
```
