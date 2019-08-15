# AMD - Arduino Matplotlib DataScience
## DataScience_Function: densePop()
___
___
# densePop():- **`Returns a hybrid`**
#### This function takes a hybrid and gives us the most densely populated region.
#### **`densePop( hyb )`** is the function header.
## Eg:
```python
from AMD import *

y = [33,34,33.5,32,34,33.6,33.2,33,9,33,7,34,32.7]
# y contains a list of amplitudes that are closely packed

from random import randint as ri

for _ in range(20):
    y.insert(ri(0,20),ri(0,70))
# insert 20 random values at random positions in the list y
print(y)
# the randomizing block gave me this list
# [33, 32, 64, 67, 4, 34, 32, 47, 33.5, 26, 32, 46, 34, 51,
# 68, 23, 58, 33.6, 33.2, 11, 17, 33, 53, 33, 9, 23, 33, 65,
# 7, 34, 25, 38, 32.7]

hyb = hybridize(y)
# hybridizing y to work with AMD functions

denseHyb = densePop(hyb)
# denseHyb contains the most densely populated
# region of hyb which is essentially between 32
# and 34 as in the first version of y !

compGraph(hyb,denseHyb)
```
### Resulting Graph:
#### If you want to filter out the impulses further you can use the same function again or use cleanImpulses().
![densePop](https://github.com/SayadPervez/Arduino_Master_Delta/blob/master/densePop.png?raw=true)
___
___
![Mr_Handsome](https://github.com/SayadPervez/AMD-SEPERATE-DOCUMENTATION/blob/master/IMG_20190225_150001_460.jpg?raw=true)
### Sayad Pervez - the solo developer of AMD Module !
### E-Mail : [pervez2504@gmail.com](pervez2504@gmail.com)
___
___
