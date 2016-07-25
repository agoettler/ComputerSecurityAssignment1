Andrew Goettler
Computer Security Spring 2016
Assignment 1

Description:

For assignment 1, I implemented the Vigenèr cipher and the permutation cipher
in Python 3.5.1.

The implementation of the Vigenèr cipher takes advantage of the numerical
properties of ASCII character encodings. Converting each lower-case letter into
an integer and subtracting 97 results in an integer representation in the range
of 0-25, handy for executing shift ciphers. After ciphering, the
conversion process is reversed to produce valid ASCII characters again.

The implementation of the permutation cipher makes use of Python's powerful and
convenient lists. However, there is some inelegant code required to preserve
spaces in the ciphertext, not a usual feature of permutation ciphers.

Instructions:

This code was written for Python 3.5.1. All code for this assignment is
contained in the "assignment1.py" file. 

The "simpleVigenerEncrypt" takes a string representing the key, a string
representing the filename of a text file for input, and a string representing
the filename of a text file for ouput.

The "simplePermutationEncrypt" functions similarly, but requires a Python list
of consecutive, 1-indexed integers as a key.

To use these functions, start a Python interpreter session and import the
"assignment1" module. The functions can then be executed just like functions
in any Python module, 
ex. "assignment1.simpleVigenerEncrypt("key", "input.txt", "ouput.txt").

To produce the included output ciphertexts, simply execute the 
"testEncryptions()" function.

Examples:

"plaintext1.txt" is an excerpt from J.R.R Tolkien's "The Lord of the Rings".
"plaintext2.txt" is an excerpt from Edgar Allan Poe's "The Telltale Heart".

"simpleVigenerCiphertext.txt" is encrypted from "plaintext1.txt" using the
Vigenèr cipher with the key "rohan", with spaces left in the ciphertext.

"completeVigenerCiphertext.txt" is encrypted from "plaintext2.txt" using the
Vigenèr cipher with the key "heart", with spaces removed from the ciphertext.

"simplePermutationCiphertext.txt" is encrypted from "plaintext1.txt" using the
permutation cipher with the key [6, 5, 4, 3, 2, 1], with spaces left in
the ciphertext.

"completePermutationCiphertext.txt" is encrypted from "plaintext2.txt" using
the permutation cipher with the key [2, 5, 3, 1, 6, 4], with spaces removed
from the ciphertext.
