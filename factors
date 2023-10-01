#!/usr/bin/python3
"""
Factorize as many numbers as possible into a product of two smaller numbers.

Functions:
    find_divisor(num) -> int
    factorize()

Usage: ./factors <file>
    Where <file> is a file containing natural numbers to factor.
    One number per line.
Output format: n=p*q
    One factorization per line.
    p and q are not always prime numbers.
"""

import sys


def find_divisor(num: int) -> int:
    """
    Finds the smallest divisor of a given number.
    Args:
        num (int): A number to find the smallest divisor for.
    Returns:
        smallest divisor if found
        0 if the number is prime
    """

    while num % 2 == 0:
        return 2

    factor = 3
    while factor * factor <= num:
        if num % factor == 0:
            return factor
        else:
            factor += 2

    return 1


def factorize():
    """
    Factorizes as many numbers as possible into
    a product of two smaller numbers and print them.
    """

    with open(sys.argv[1]) as f:
        line = f.readline()
        while line != '':
            num = int(line)
            div = find_divisor(num)
            print(f"{num}={num//div}*{div}")

            line = f.readline()


if __name__ == "__main__":
    factorize()
