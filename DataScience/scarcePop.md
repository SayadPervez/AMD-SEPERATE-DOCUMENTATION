# AMD - Arduino Matplotlib DataScience
## DataScience_Function: scarcePop()
___
___
# scarcePop():- **`Returns a Hybrid`**
#### This function takes a hybrid and gives us the least densely populated region.
#### **`scarcePop( hyb )`** is the function header.
## Eg:
```python
from AMD import *

y = [33, 32, 64, 67, 4, 34, 32, 47, 33.5, 26, 32, 46, 34, 51, 68, 23, 58, 33.6, 33.2, 11, 17, 33, 53, 33, 9, 23, 33, 65, 7, 34, 25, 38, 32.7]
# lets use the list randomly generated in the previous example !

hyb = hybridize(y)
# hybridizing y to work with AMD functions

scarceHyb = scarcePop(hyb)
# scarceHyb contains the least densely populated
# region of hyb which essentially excludes region between 32
# and 34 !

compGraph(hyb,scarceHyb)
```
### Resulting Graph:
![scarcePop](https://github.com/SayadPervez/Arduino_Master_Delta/blob/master/scarcePop.png?raw=true)
___
___
![Mr_Handsome](https://github.com/SayadPervez/AMD-SEPERATE-DOCUMENTATION/blob/master/IMG_20190225_150001_460.jpg?raw=true)
### Sayad Pervez - the solo developer of AMD Module !
### E-Mail : [pervez2504@gmail.com](pervez2504@gmail.com)
___
___
