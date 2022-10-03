# 1.18-notes

## Pseudorandom numbers

- Pseudorandom numbers - when algorithms create long runs of numbers that are relatively random but eventually repeat. Most computer generated random numbers use them. (PRNGs)

- Adequaqte for situations like computer simulations and cryptography.

- Aren't as random as coin tosses + dice rolls.

- Generate a random sequence - determined by shorter intial value aka seed value or key.

- As a result, the sequence that seems random can be reproduced if the seed value is known.

In the linear congruential method the next number in the pseudorandom sequence is calculated from its immediate predecessor as follows:

next = (multiplier * predecessor + increment) MOD modulus

Multiplier = 13, Increment = 0, Modulus = 31

When predecessor = 1, sequence is

1, 13, 14, 27, 10, 6, 16, 22, 7, 29, 5, 3, ...

First thirty terms in this sequence are a permutation of the integers 1 to 30 and then the sequence repeats itself. It has a period equal to modulus -1.

The starting value is called the seed.

## Mersenne Twister

The Mersenne Twister is a general-purpose pseudorandom number generator developed in 1997 by Makoto Matsumoto and Takuji Nishimura. Its name derives from the fact that its period length is chosen to be a Mersenne prime. The Mersenne Twister was designed specifically to rectify most of the flaws found in older PRNGs. The standard implementation uses a 32-bit word length.
