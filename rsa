#!/usr/bin/env python3
import sys

def is_prime(num):

    if num > 1:
        for d in range(2, num):
            if num % d == 0:
                return False
        return True
    return False


def factor(n):

    if n < 2:
        return False
    for p in range(2, n):
        if n % p == 0:
            q = n // p
            if is_prime(p) and is_prime(q):
                print("{} = {} * {}".format(n, p, q))
                return True
    return False


def main(file_path):

    with open(file_path, 'r') as file:
        for line in file:
            num = int(line.rstrip())
            factor(num)


if __name__ == "__main__":
    if len(sys.argv) != 2:
        print("Usage: factors <file>")
        sys.exit(1)
    main(sys.argv[1])
