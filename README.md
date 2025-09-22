# Huffman Shannon Fano
# Aim:
Consider a discrete memoryless source with symbols and statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} for its output. 
Apply the Huffman and Shannon-Fano to this source. 
Show that by drawing the tree diagram, and 
Calculate the average code word length, entropy, variance, redundancy, and efficiency.
# Tools Required:
# Program:
```
import math

p = [0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25]
lk = [3, 4, 2, 4, 3, 3, 2]
n = len(p)

L = sum(p[k] * lk[k] for k in range(n))
hs = sum(p[k] * math.log(1 / p[k], 2) for k in range(n))
hs = round(hs, 3)

eff = round(hs / L, 3)
red = round(1 - eff, 3)

var = sum(p[k] * (lk[k] - L) ** 2 for k in range(n))
var = round(var, 3)

print(f"Average Codeword Length is : {L}")
print(f"Entropy is : {hs}")
print(f"Efficiency is : {eff * 100}%")
print(f"Redundancy is : {red}")
print(f"Variance is : {var}")

```
# Calculation:
```
Compare the manually calculated value and the observed practical value.
```
# Output
```
Average Codeword Length is : 2.625
Entropy is : 2.625
Efficiency is : 100.0%
Redundancy is : 0.0
Variance is : 0.484

``` 
# Results:
```
The Parameters are Calculated
```
