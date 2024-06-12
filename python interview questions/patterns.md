# Patterns

## Pattern Printing Using Loops

### 1. Solid Rectangle

```
*****
*****
*****
*****
*****
```

```python
def solid_rectangle(rows, cols):
    for i in range(rows):
        print("*" * cols)
```

### 2. Right Triangle

```
*
**
***
****
*****
```

```python
def right_triangle(n):
    for i in range(1, n+1):
        print("*" * i)
```

### 3. Inverted Right Triangle

```
*****
****
***
**
*
```

```python
def inverted_right_triangle(n):
    for i in range(n, 0, -1):
        print("*" * i)
```

### 4. Incremental Numbers

```
1
1 2
1 2 3
1 2 3 4
1 2 3 4 5
```

```python
def incremental_numbers(n):
    for i in range(1, n+1):
        for j in range(1, i+1):
            print(j, end=" ")
        print()
```

### 5. Pyramid with Base on Both Ends

```
*
**
***
****
*****
****
***
**
*
```

```python
def pyramid_base_both_ends(n):
    for i in range(1, n+1):
        print("*" * i)
    for i in range(n-1, 0, -1):
        print("*" * i)
```

### 6. Right-Aligned Right Triangle

```
    *
   **
  ***
 ****
*****
```

```python
def right_aligned_right_triangle(n):
    for i in range(1, n+1):
        print(" " * (n-i) + "*" * i)
```

### 7. Right-Aligned Inverted Right Triangle

```
*****
 ****
  ***
   **
    *
```

```python
def right_aligned_inverted_right_triangle(n):
    for i in range(n, 0, -1):
        print(" " * (n-i) + "*" * i)
```

### 8. Centered Triangle

```
    *
   ***
  *****
 *******
*********
```

```python
def centered_triangle(n):
    for i in range(1, n+1):
        print(" " * (n-i) + "*" * (2*i-1))
```

### 9. Centered Inverted Triangle

```
*********
 *******
  *****
   ***
    *
```

```python
def centered_inverted_triangle(n):
    for i in range(n, 0, -1):
        print(" " * (n-i) + "*" * (2*i-1))
```

### 10. Hollow Pyramid

```
    *
   * *
  * * *
 * * * *
* * * * *
```

```python
def hollow_pyramid(n):
    for i in range(n):
        print(" " * (n-i-1) + "*", end="")
        if i >= 1:
            print(" " * (2*i-1) + "*", end="")
        print()
```

### 11. Hollow Inverted Pyramid

```
* * * * *
 * * * *
  * * *
   * *
    *
```

```python
def hollow_inverted_pyramid(n):
    for i in range(n):
        print(" " * i + "*", end="")
        if i < n-1:
            print(" " * (2*(n-i-1)-1) + "*", end="")
        print()
```

### 12. Combined Pyramids

```
* * * * *
 * * * *
  * * *
   * *
    *
    *
   * *
  * * *
 * * * *
* * * * *
```

```python
def combined_pyramids(n):
    hollow_pyramid(n)
    hollow_inverted_pyramid(n)
```

### 13. Hollow Diamond

```
    *
   * *
  *   *
 *     *
*********
```

```python
def hollow_diamond(n):
    for i in range(n-1):
        print(" " * (n-i-1) + "*", end="")
        if i >= 1:
            print(" " * (2*i-1) + "*", end="")
        print()
    for i in range(n):
        print(" " * i + "*", end="")
        if i < n-1:
            print(" " * (2*(n-i-1)-1) + "*", end="")
        print()
```

### 14. Hollow Inverted Diamond

```
*********
 *     *
  *   *
   * *
    *
```

```python
def hollow_inverted_diamond(n):
    for i in range(n):
        print(" " * (n-i-1) + "*", end="")
        if i >= 1:
            print(" " * (2*i-1) + "*", end="")
        print()
    for i in range(n-1):
        print(" " * i + "*", end="")
        if i < n-2:
            print(" " * (2*(n-i-2)-1) + "*", end="")
        print()
```

### 15. Full Diamond

```
    *
   * *
  *   *
 *     *
*       *
 *     *
  *   *
   * *
    *
```

```python
def full_diamond(n):
    hollow_diamond(n)
    hollow_inverted_diamond(n)
```

### 16. Pascal's Triangle

```
        1
      1   1
    1   2   1
  1   3   3   1
1   4   6   4   1
```

```python
def pascals_triangle(n):
    for i in range(n):
        for j in range(n-i-1):
            print(" ", end="")
        val = 1
        for j in range(i+1):
            print(val, end=" ")
            val = val * (i - j) // (j + 1)
        print()
```

### 17. Centered Numeric Pyramid

```
    1
   212
  32123
 4321234
  32123
   212
    1
```

```python
def centered_numeric_pyramid(n):
    for i in range(1, n+1):
        print(" " * (n-i) + " ".join(str(j) for j in range(i, 0, -1)) + " " + " ".join(str(j) for j in range(2, i+1)))
    for i in range(n-1, 0, -1):
        print(" " * (n-i) + " ".join(str(j) for j in range(i, 0, -1)) + " " + " ".join(str(j) for j in range(2, i+1)))
```

### 18. Hollow Square with Cross

```
**********
****  ****
***    ***
**      **
*        *
*        *
**      **
***    ***
****  ****
**********
```

```python
def hollow_square_with_cross(n):
    for i in range(n):
        if i == 0 or i == n-1:
            print("*" * (2*n))
        else:
            print("*" + " " * (2*n-2) + "*")
    mid = n // 2
    for i in range(n):
        if i == mid:
            print("*" * mid + " " * (n-2) + "*" * mid)
        else:
            print(" " * mid + "*" + " " * (n-2) + "*" + " " * mid)
```

### 19. Hourglass

```
*        *
**      **
***    ***
****  ****
**********
****  ****
***    ***
**      **
*        *
```

```python
def hourglass(n):
    for i in range(n):
        print("*" * i + " " * (2*(n-i)) + "*" * i)
    print("*" * n * 2)
    for i in range(n-1, -1, -1):
        print("*" * i + " " * (2*(n-i)) + "*" * i)
```

### 20. Hollow Rectangle

```
****
*  *
*  *
*  *
****
```

```python
def hollow_rectangle(rows, cols):
    for i in range(rows):
        if i == 0 or i == rows-1:
            print("*" * cols)
        else:
            print("*" + " " * (cols-2) + "*")
```

### 21. Incremental Numbers in Rows

```
1
2  3
4  5  6
7  8  9  10
11 12 13 14 15
```

```python
def incremental_numbers_in_rows(n):
    num = 1
    for i in range(1, n+1):
        for j in range(1, i+1):
            print(num, end=" ")
            num += 1
        print()
```

### 22. Alternating Binary Numbers

```
1
0 1
1 0 1
0 1 0 1
1 0 1 0 1
```

```python
def alternating_binary_numbers(n):
    for i in range(1, n+1):
        for j in range(1, i+1):
            print((i+j) % 2, end=" ")
        print()
```

### 23. Star Pattern with Spaces

```
    *      *
  *   *  *   *
*      *      *
```

```python
def star_pattern_with_spaces(n):
    for i in range(n):
        print(" " * (n-i-1) + "*" + " " * (2*i) + "*" + " " * (2*(n-i-1)) + "*" + " " * (2*i) + "*")
```

### 24. Star Cross Pattern

```
*        *
**      **
* *    * *
*  *  *  *
*   **   *
*   **   *
*  *  *  *
* *    * *
**      **
*        *
```

```python
def star_cross_pattern(n):
    for i in range(n):
        if i == 0 or i == n-1:
            print("*" * (2*n))
        else:
            print("*" + " " * (i-1) + "*" + " " * (2*(n-i)-1) + "*" + " " * (2*(n-i)-1) + "*" + " " * (i-1) + "*")
```

### 25. Hollow Square with Border

```
    *****
   *   *
  *   *
 *   *
*****
```

```python
def hollow_square_with_border(n):
    for i in range(n):
        if i == 0 or i == n-1:
            print(" " * (n-1) + "*" * n)
        else:
            print(" " * (n-i-1) + "*" + " " * (n-2) + "*")
```

### 26. Repeated Numbers

```
1 1 1 1 1 1
2 2 2 2 2
3 3 3 3
4 4 4
5 5
6
```

```python
def repeated_numbers(n):
    for i in range(1, n+1):
        print((str(i) + " ") * (n-i+1))
```

### 27. Numbers with Decreasing and Increasing Length

```
1 2 3 4  17 18 19 20
  5 6 7  14 15 16
    8 9  12 13
      10 11
```

```python
def numbers_with_decreasing_and_increasing_length(n):
    num = 1
    for i in range(n):
        print("  " * i, end="")
        for j in range(n-i):
            print(num, end=" ")
            num += 1
        num -= 1
        for j in range(n-i-1):
            num -= 1
            print(num, end=" ")
        print()
```

### 28. Diamond of Stars

```
    *
   * *
  * * *
 * * * *
* * * * *
 * * * *
  * * *
   * *
    *
```

```python
def diamond_of_stars(n):
    for i in range(n):
        print(" " * (n-i-1) + "*" * (2*i+1))
    for i in range(n-2, -1, -1):
        print(" " * (n-i-1) + "*" * (2*i+1))
```

### 29. Hourglass with Stars

```
*        *
**      **
***    ***
****  ****
**********
****  ****
***    ***
**      **
*        *
```

```python
def hourglass_with_stars(n):
    hourglass(n)
    print()
    hourglass(n)
```

### 30. Pyramid with Numbers

```
        1
      2 1 2
    3 2 1 2 3
  4 3 2 1 2 3 4
5 4 3 2 1 2 3 4 5
```

```python
def pyramid_with_numbers(n):
    for i in range(1, n+1):
        print(" " * (n-i), end="")
        for j in range(i, 0, -1):
            print(j, end="")
        for j in range(2, i+1):
            print(j, end="")
        print()
```

### 31. Concentric Squares

```
4 4 4 4 4 4 4  
4 3 3 3 3 3 4   
4 3 2 2 2 3 4   
4 3 2 1 2 3 4   
4 3 2 2 2 3 4   
4 3 3 3 3 3 4   
4 4 4 4 4 4 4   
```

```python
def concentric_squares(n):
    for i in range(n):
        for j in range(n):
            print(max(i, j, n-i-1, n-j-1) + 1, end=" ")
        print()
```

### 32. Alphabetical Incremental

```
E
D E
C D E
B C D E
A B C D E
```

```python
def alphabetical_incremental(n):
    for i in range(n):
        for j in range(i+1):
            print(chr(65+n-j-1), end=" ")
        print()
```

### 33. Alphabetical Alternating Cases

```
a
B c
D e F
g H i J
k L m N o
```

```python
def alphabetical_alternating_cases(n):
    for i in range(n):
        for j in range(i+1):
            if (i+j) % 2 == 0:
                print(chr(97+j+(i-j)), end=" ")
            else:
                print(chr(65+j+(i-j)), end=" ")
        print()
```

### 34. Inverted Alphabetical

```
E D C B A
D C B A
C B A
B A
A
```

```python
def inverted_alphabetical(n):
    for i in range(n):
        for j in range(n-i):
            print(chr(65+n-j-i-1), end=" ")
        print()
```

### 35. Numbers with Symmetry

```
1      1
12    21
123  321
12344321
```

```python
def numbers_with_symmetry(n):
    for i in range(1, n+1):
        for j in range(1, n*2+1):
            if j <= i or j >= 2*n+1-i:
                print(j, end=" ")
            else:
                print(" ", end=" ")
        print()
```
