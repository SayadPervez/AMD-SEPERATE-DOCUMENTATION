# AMD - Arduino Matplotlib DataScience
## DataScience_Function: visualizeSmoothie()
___
___
# visualizeSmoothie():- **`Returns a Hybrid`**
#### **`visualizeSmoothie( hyb, equiAxis = False )`** is the function header.
#### This function plots all the smoothies with levels from 0 to ((number of index values) - 1)
#### It indeed gives a beautiful pattern as in the introductory pic of this module !

|Parameter|Usage|
|---|---|
| equiAxis = False | To specify whether the axes units should be exact. [Learn More here](https://github.com/SayadPervez/Arduino_Master_Delta/blob/master/equiaxis.md)|

## Eg:
```python
from AMD import *
y = [33, 32, 64, 67, 4, 34, 32, 47, 33.5, 26, 32, 46, 34, 51, 68, 23, 58, 33.6, 33.2, 11, 17, 33, 53, 33, 9, 23, 33, 65, 7, 34, 25, 38, 32.7]
# lets use the list randomly generated in the previous example !

from random import randint as ri

for i in range(30):
    y.insert(ri(0,30),ri(0,70))

# adding 30 more random values to y

hyb = hybridize(y)
# hybridizing y to work with AMD functions

visualizeSmoothie(hyb)
```
### Resultant Graph:
![visSm](https://github.com/SayadPervez/Arduino_Master_Delta/blob/master/vissm.jpeg?raw=true)
___
___
![Mr_Handsome](https://github.com/SayadPervez/AMD-SEPERATE-DOCUMENTATION/blob/master/IMG_20190225_150001_460.jpg?raw=true)
### Sayad Pervez - the solo developer of AMD Module !
### E-Mail : [pervez2504@gmail.com](pervez2504@gmail.com)
___
___
