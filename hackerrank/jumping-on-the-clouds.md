https://www.hackerrank.com/challenges/jumping-on-the-clouds/problem

```python
#!/bin/python3

import math
import os
import random
import re
import sys

# Complete the jumpingOnClouds function below.
def jumpingOnClouds(c):
    count, i = 0, 0
    while i < len(c)-1:
        if i+2 < len(c) and c[i+2] != 1:
            i += 1
        count += 1
        i += 1
    return count

if __name__ == '__main__':
    fptr = open(os.environ['OUTPUT_PATH'], 'w')

    n = int(input())

    c = list(map(int, input().rstrip().split()))

    result = jumpingOnClouds(c)

    fptr.write(str(result) + '\n')

    fptr.close()
```