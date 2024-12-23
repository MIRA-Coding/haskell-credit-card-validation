# Luhn Algorithm for Credit Card Validation 🔍🧮

## Overview
The **Luhn algorithm**, also known as the **modulus 10** or **mod 10** algorithm, is a simple checksum formula used to validate various identification numbers, most notably credit card numbers. This project implements the Luhn algorithm to validate credit card numbers and provides a detailed explanation of how the algorithm works.

## How the Luhn Algorithm Works
The Luhn algorithm checks whether a given credit card number is valid by performing the following steps:

1. **Reverse the Credit Card Number**:
   - Start with the rightmost digit (check digit) and move left.
   
2. **Double Every Second Digit**:
   - Beginning with the first digit on the right, double the value of every second digit.
   - If doubling a digit results in a two-digit number (e.g., 7 × 2 = 14), add the digits of the product together (e.g., 1 + 4 = 5).

3. **Sum All Digits**:
   - Add all the single digits obtained from the above step to the digits that were not doubled.

4. **Check the Total**:
   - If the total modulo 10 equals 0, the credit card number is valid; otherwise, it is invalid.

### Example
For the credit card number **4539 1488 0343 6467**:
1. Reverse: `7 6 4 6 3 4 3 0 8 8 4 9 3 5 4`.
2. Double every second digit: 7, (6×2=12), 4, (6×2=12), 3, (4×2=8), 3, (0×2=0), 8, (8×2=16), 4, (9×2=18), 3, (5×2=10), 4
3. Replace double-digit results with their digit sums: 7, 3, 4, 3, 3, 8, 3, 0, 8, 7, 4, 9, 3, 1, 4
4. Sum all digits: 7 + 3 + 4 + 3 + 3 + 8 + 3 + 0 + 8 + 7 + 4 + 9 + 3 + 1 + 4 = 69
5. Check total:
- `69 % 10 = 9` (Invalid card number).
