Notes
=====

## /10/11

I started these notes slightly late, after Shai told me I might want to log not only my thought but also the material I'm learning so I can refer back to it at a later point.

### Substitution Cipher /03

A _substitution cipher_ is a cipher in which each letter is substituted with another letter (or other type of symbol).

These ciphers can be relatively easy to break calculating the statistically frequency of the letters in the english as well a certain combinations of letters such as q being followed by u. 

### Number Theory

Number theory is the study of natural numbers, or more generally integers. The integers are denoted by the blackboard Z character. 

	-∞ … -3, -2, -1, 0, 1, 2, 3, … ∞

The integers are considered a ring because an addition, subtraction or multiplication of any two numbers within the integers yields an integer. However, division does not allows us always stay within the integers, e.g.: `3/2 = 1.5`. 

### Divisibility

We say two integers, `b` and `a`, divide if there is an integer `c` such that:

	b = ac

This is written as `a|b`. In-divisibility is written as `a∤b`. Main ideas:

	a|b, b|c => a|c
	a|b, b|a => a = ±b
	a|b, a|c => a|(b+c), a|(b-c)
	a|b, a > 0, b > 0 => a ≤ b
	m∤0 => a|b <=> ma|mb

### GCD - Greatest Common Divisor

The GCD of two numbers is the largest positive integer `d`, such that `a|d` and `b|d` hold true. This is denoted as `gcd(a,b)`.

### Euclidean Algorithm /05

This is the most efficient algorithm to find the GCD of two numbers.

To efficiently find the GCD of two numbers begin the with a simple divisibility statement `a|b`:

	b = a*q + r

Then continue to open the equation for `a` using `r`, as such:

	b = a*q + r[2]
	a = r[2]*q[2] + r[3]
	r[2] = r[3]*q[3] + r[4]
			…
	r[t-1] = r[t]*q[t]

Until the remainder, `r` is 0. The GCD is then the `a` value, or `r[t]`.

This works out because the algorithm is essentially in the form:
	
	r[i−1] = r[i]*q[i] + r[i+1]

This implies that any common divisor of `r[i-1]` and `r[i]` is also a divisor of `r[i+1]`, and similarly that any common divisor of `r[i+1]` and `r[i]` is also a divisor of `r[i-1]`. Therefore:

	gcd(r[i-1],r[i]) = gcd(r[i],r[i+1])							…
	gcd(r[t-1],r[t]) = gcd(r[t],r[t+1])
	∴ gcd(r[t],r[t+1]) = gcd(a,b)

This is a finite algorithm that takes at most `2log2(b) + 1` calculations to terminate.

### Extended Euclidean Algorithm

This is basically a rearrangement of the Euclidean algorithm, stating that there is for `a` and `b` in the equation:

	au + bv = gcd(a,b)

There is always a solution to `u` and `v`. This is particularly useful when `a` and `b` are relatively prime, as it finds `u` and `v`. `u` is the multiplicative inverse of `a mod b` and `v` is inverse of `b mod a`. To find the values of `u` and `v`, first solve the Euclidean Algorithm

	a = 73, b = 25

	73 = 25 * 2 + 23
	25 = 23 * 1 + 2
	23 = 2 * 11 + 1
	2 = 1 * 2 + 0

Then create a box, as such:

	         2   1   11  2
	------------------------
	|0 | 1 | * | * | * | * |
	------------------------
	|1 | 0 | * | * | * | * |
	------------------------

Where the first two numbers are always 0, 1 and 1, 0 and the numbers above are the quotients of the Euclidean Algorithm. Each new entry can be filled out using the rule:

	New = (Top * Left) + (2 Spaces Left)  
 
Therefore, the above chart fills out into:

	         2   1   11   2
	--------------------------
	|0 | 1 | 2 | 3 | 35 | 73 |
	--------------------------
	|1 | 0 | 1 | 1 | 12 | 25 |
	--------------------------

Notice that the last two numbers are `a` and `b` respectively. More importantly, however, is that the second last column yields the `-v` and `u` values (in that order). Therefore:

	       	q[i] ------> q[t]
	-------------------------
	|0 | 1 | * | * | -v | a |
	-------------------------
	|1 | 0 | * | * |  u | b |
	-------------------------

Whenever, the `gcd(A,B) = 1`, the two integers `A` and `B` can be considered relatively prime and therefore:

	au + bv = 1 

Where `a = A/gcd(A,B)` and `b = B/gcd(A,B)`.

### Modular Arithmetic

Modular arithmetic is basically division, except you don't care about the quotient, only the remainder.

More formally:

If `m` ≥ 1, we say `a` and `b` are congruent modulo if the difference between `a` and `b` is divisible by `m`. This is written:

	a ≡ b (mod m)

Which can also be represented as:

	a = b * q + r => a - r = bq => a ≡ r (mod b)

Numbers satisfying `a ≡ 0 (mod m)` indicate that they are multiples of `a`.

Some modulo ground rules, if `a[1] ≡ a[2] (mod m)` and `b[1] ≡ b[2] (mod m)`, then:

	a[1] ± b[1] ≡ a[2] ± b[2] (mod m)
	a[1] * b[1] ≡ a[2] * b[2] (mod m)

Furthermore:

	a * b = 1 (mod m) <=> gcd(a,m) = 1

If the integer `b` exits in the equation above, it is called the _inverse modulo_ `a` of `m`. For example:

	m = 5
	a = 2

	2 * b ≡ 1 (mod 5) as gcd(2,5) = 1
	
	b = 3
	a^-1 = 3 (mod 5)

	Check: 2 * 3 ≡ 1 (mod 5)

The inverse modulo can be solved for by rearranging the formula above, into the form of the Extended Euclidean Algorithm.

	a * b = 1 (mod m)
	a * b - 1 = 0 (mod m)
	(a * b) - 1 = m *I think…*
	ab - m = 1 *I think…*

For example:

	m = 5
	a = 2

	2b - 1 = 0 (mod 5)
	2b - 1 = 5
	2b = 6
	b = 3
	

### Modulo Rings /13

If we are interested in integers modulo `m`, we can can use the integers from 0 to `m - 1` which we get from `a ≡ r (mod m)`. This is called a _ring of integers modulo_ `m`, and is expressed with the following notation:

	Z/mZ = {0, 1, 2, … m-1}

Note that whenever addition or multiplication in the ring `Z/mZ`, the result is always divided by `m` and the remainder is taken to return a value in the ring `Z/mZ`.

### Unit Modulo Rings 

Numbers which have an inverse modulo, and therefore have `gcd(a,b) = 1` are called units. A sets of units are called a _unit modulo ring_ and are denoted like this:

	(Z/mZ)* = {a ∈ Z/mZ, gcd(a,m) = 1}
	
Which can also be called a subset of `Z/mZ` of integers relatively prime to `m`. Notice that multiplication between unit values always yields a unit value (remember to divide by m and take the remainder).

Euler's phi function is defined to return the number of elements in the set `(Z/mZ)*`.

	ϕ(m) = n((Z/mZ)*) 
			= n({0 ≤ a < m, gcd(a,m) = 1})

### Modular Arithmetic & Shift Ciphers

A shift cipher can be mathematically modelled using modular arithmetic.

	c = integer cipher letter
	p = integer plain text letter

	k = secret integer key

	c ≡ p+k (mod 26) <-Encryption
	p ≡ c-k (mod 26) <-Decryption

### Fast Powering Algorithm

The Fast Powering Algorithm allows us to quickly and efficiently compute `g` to the power of large values `A` modulo `N`. This can be expressed as: 
	
	g^A (mod m)

Obviously, the answer can be naïvely obtained by multiplying `g`, however this is highly inefficient. The algorithm breaks `A` down into a succession of squares and simpler multiplications.

Begin by breaking `A` down into powers of 2. 

	A = A[0] + A[1] * 2 + A[2] * 2^2 … + A[r]*2^r

	Such that A[r] ∈ {0, 1} and assuming A[r] = 1

Then compute the values of `g^A[i]` while 0 ≤ `i` ≤ `r` using successive squaring.

Then simply multiply together all of the values of `g` and divide by `m` at each multiplication. 

This algorithm takes at most `2log2(A)` multiplications to find `g^A`, which several times better than the naïve approach. 

### Prime Numbers

It is only possible to divide `a` in the ring `Z/mZ` if `gcd(a,m) = 1`. Therefore, instances where `m` is prime mean that every number will be divisible by `a`.

An integer `p` ≥ 2 is called prime when the only positive integers dividing `p` are 1 and `p`.

Firstly, we state that if `p` divides `a[1]a[2]a[n]` then `p` must divide at least one of `a[i]`. Which leads to our proof that every integer has a unique factorization of primes. 

Suppose `a` can be factorized into two products of primes:

	a = p[1]p[2]p[3]p[i] = q[1]q[2]q[3]q[t]

Thus, based on the above proposition, we find that `p[1]` must divide at least one of `q[i]`, and since `p[1]` is prime, the values of `q[i]` it divides must be equivalent to itself. `p[1]` and (assuming rearrangement) `q[1]` can cancel out. Hence, we see that this number only has one unique combination of primes that make up it's factorization.

We use the `ordp(a)` notation to describe the power prime `p` is taken to in the prime factorization of `a`, or the *order of `p` in `a`*. For example:

	1728 = 2^6 * 3^3

	ord2(1728) = 6 and ord3(1728) = 3

Returning to the idea of divisibility in the ring `Z/pZ`, we can say that the ring `(Z/pZ)*` of any prime will be a fully commutative ring, which means it supports addition, subtraction, multiplication and division throughout. This is called a _field_, and because, unlike other fields such as the `R`'s and the `Q`'s, it is finite, we denote this as `Fp`, similarly, we write `Fp*` to indicate a unit group, identical to `(Z/pZ)*`. 

### Fermat's Little Theorem

Let `p` be a prime number and let `a` be any integer. Then, `a` taken to the power `p - 1` is said to yield:

					{ 1 (mod p), a∤p
	a^(p-1) ≡ 	|
					{ 0 (mod p), a|p 


This theorem, called _Fermat's Little Theorem_ allows us to quickly identify if a number is a multiple of another. e.g.: 2^15485862 − 1 is a multiple of 15485863 as:

	2^15485862 - 1 ≡ 1 (mod 15485863)

We can also use this theorem in combination with the Fast Powering Algorithm to quickly find the inverse modulo of an integer `a`, providing an alternative to the Extended Euclidean Algorithm:

	a^-1 ≡ a^(p-2) (mod p)

For examples the inverse 7814 modulo 17449 can be calculated as such:

	7814^−1 ≡ 7814^17447 ≡ 1284 (mod 17449).

Although Fermat's' Theorem tells us that for any `a` not divisible by `p`, the value of `a^(p-1)` will be modulo to `p`, it does not state that this power of `a` is the lowest power that is modulo `p` equal to 1. We therefore define the order of `a` modulo `p` as the smallest power `k` which `a` needs to be taken to, to yield modulo `p` 1.

	a^k ≡ 1 (mod p)

Based on this, we can say that if an integer `a` is not divisible by `p` and `a^n ≡ 1 (mod p)`. Then the order of modulo `p` divides `n` and the order of `a` divides `p-1`.

### Primitive Roots Theorem

Let `p` be a prime number. Then there exists an element `g` of `Fp*`, whose powers give every element of `Fp*`. e.g.:

	Fp* = {1,g^2, g^3, g^4 … g^(p-2)}

Elements which have such properties are called _primitive roots_  of `Fp` and  _generators_ of `Fp*`. They are elements of `Fp*` which have order `p-1`. For example the field `F11*` has the primitive root of 2 as:

	2^0 = 1  2^1 = 2 2^2 = 4 2^3 = 8 2^4 = 5 	2^5 = 10 2^6 = 9 2^7 = 7 2^8 = 3 2^9 = 6

As numbers get larger, there can be quite a few primitive roots. The precise formula says that `Fp` has exactly `ϕ(p − 1)` primitive roots.

### Symmetric Ciphers

In a symmetric cipher based crypto system, both Alice and Bob would need to have knowledge of a secret key, `k`, which they would use to encrypt and decrypt. It is called a symmetric cipher because both Alice and Bob must have the same encryption, decryption and key to exchange information securely.

This can also be expressed mathematically, where sets `K`, `M` and `C` are sets of all possible keys, messages and cipher texts respectively. As such, encryption can be seen as a function,

	e: K x M -> C

Whose domain `K x M` is a set of pairs `(k,m)`, whose range is in the space `C`. Similarly, decryption is the function,

	d: K x C -> M

Of course, we would like encryption and decryption to "undo" each other, which is expressed as:

	d(k,e(k,m)) = m for all k ∈ K and all m ∈ M
	
It is sometimes convenient to write the dependancy on the key `k` as a subscript, (or in this case an member):

	e[k]: M -> C
	
	d[k]: C -> M

It is important to note that the function `e[k]()` must map an input to an output in a one-to-one fashion.

It is safest to assume that Eve knows the encryption method that is being employed, or functions `e()` and `d()`. This is based on _Kerckhoff’s principle_, which states the security of a crypto system should be based on it's secret key alone, not the secrecy of the algorithm.

If any cipher is to be successful for `(K,M,C,e(),d())`, it must have the following properties:

- For any key `k ∈ K` and plaintext `m ∈ M`,it must be easy to compute the ciphertext `e[k](m)`.
- For any key `k ∈ K` and ciphertext `c ∈ C`, it must be easy to compute the plaintext `d[k](c/)`.
- Given one or more ciphertexts `c[1], c[2] , … c[n] ∈ C` encrypted using the key `k ∈ K`, it must be very difficult to compute any of the corresponding plaintexts `d[k](c[1]), … d[k](c[n])` without knowledge of `k`.
	
- Given one or more pairs of plaintexts and their corresponding ciphertexts, `(m[1],c[1]), (m[2],c[2]), … (m[n], c[n])`, it must be difficult to decrypt any ciphertext `c` that is not in the given list without knowing `k`. This is known as security against a chosen plaintext attack.

The last property is significantly more difficult to achieve. The definitions of *easy* and *hard* are left quite vague, but will be defined in later chapters.

### Encoding Schemes

An encoding scheme is a method of converting one type of data into another, for example, converting text into numbers. An encoding scheme, just like an encryption scheme, consists on encoding and decoding functions. However unlike encryption, encoding schemes are considered public, and therefore cannot hide anything. Encoding schemes should be fast and easy to compute.

Typically, ciphers work on data encoded in binary form, as this format is universally understood by all computers.

If we break the data we want to encrypt into chunks of size `B` bits, our _block size_, we can think of the sets `K`, `M`, and `C` as bounded by this size.

	K = {k ∈ Z : 0 ≤ k < 2^Bk}
	M = {m ∈ Z : 0 ≤ m < 2^Bm}
	C = {c ∈ Z : 0 ≤ c < 2^Bc}

`2^Bx` is used as the upper bound as each bit in the block size has an entropy of 2 (on|off). When we pick a `B`, therefore, we must make sure that it is large enough that Eve cannot try every element in the space. 

This method is called an _exhaustive search attack_ or _brute force attack_. These attacks are considered unfeasible after around 2^80, therefore, we must choose a `B` that is at least above 2^80. However, to prevent _collisions_, where two ciphertexts are the same with different keys, allowing the keys to be found. The recommended/safe blocksize, therefore, is at least 2^160.

### Information Theory

Information Theory defines the amount of information in a message as the minimum number of bits needed to encode all possible meanings of that message, assuming all meanings are equally likely.

The amount of information in a message `M` is measured through the entropy of `M`, denoted `H(M)`. In general, the entropy of a message is obtained by taking the log base 2 of the number of possible meanings, once again assuming each meaning is equally likely. This can be expressed as the equation:

	H(M) = log2(n)

Such that `n` is the number of possible meanings of the message. 

Entropy also measures the uncertainty of the message, ergo, the number of plaintext bits needed to be recovered from the ciphertext for the plaintext to make sense.

This can be used to explain why it's more likely that a message to Bob starts with "Dear Bob" and not "}!Q$∑'~~". 

The rate of a language is the amount of information (in bits) that is stored in each letter of the language, given as `r` by:

	r = H(M)/N

Such that `N` is the length of the message `M`. The normal rate of English is around 1.3 bits/character. That is to say, the average English message has approx. 1.3 bits of information in each character. 

The absolute rate of a language is the maximum number of bits that can be coded in each character. If there are `L` characters in a language, it is said to have an absolute rate, `R`, of:

	R = log2(L)

In English, this is around 4.7 bits/letter. However, this is not the actual rate of English, as English is highly redundant. The redundancy of English, `D`, is defined as:

	D = R - r

The redundancy of English is 3.4 bits/letter, meaning that on average, English letters have 3.4 bits of redundant or superfluous information. 

The measure of the entropy of a crypto system can be approximated by the function:

	H(K) = log2(K) 

Such that `K` is the size of the key space (ergo size of the set of all possible key values). In general, the greater the entropy of a system, the harder it is to crack. 

Cryptanalysis uses the natural redundancies of a language to reduce the number of possible plaintexts, as more than one expression can match the same meaning. The more redundant a language, the easier to analyse. This is why it is good practice to compress messages before encryption, to reduce the redundancy of the message, as well as the work required to encrypt/decrypt.

There are two basic techniques to obscure the redundancies in a plaintext message, confusion and diffusion.

Confusion obscures the relationship between the plaintext, the ciphertext and the key, making the search for redundancy and statistical patterns more difficult.

Diffusion dissipates the redundancy of the plaintext by spreading it out over the ciphertext, for example a transposition cipher like the columnar cipher simply rearranges the character of the plaintext. More advanced forms of diffusion can spread parts of the message through the entire message, rather than just transforming it.

Stream cipher use confusion only, block ciphers use both confusion and diffusion. As a rule of thumb, diffusion alone is always easily cracked.

### Theory of Block Cipher Design

The trick to a good block cipher is to mix both confusion and diffusion together in different combinations, called a product cipher. 

Block cipher that can perform these combinations of functions iteratively to a compound effect are called iterated block ciphers. Using this technique, a relatively simple confusion and diffusion combination can be compounded to achieve much stronger encryption (DES).

(page 347)

