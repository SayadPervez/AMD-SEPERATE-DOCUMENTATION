# AMD - Arduino Matplotlib DataScience
## DataScience_Function: instAvg()
___
___
# instAvg():- **`Returns a Hybrid`**
#### **`instAvg( hyb )`** is the function header.
#### This function calculates the average between every two points and returns a hybrid containing all these points. This essentially smoothens out the Graph.
## Eg:
```python
from AMD import *

y = [33, 32, 64, 67, 4, 34, 32, 47, 33.5, 26, 32, 46, 34, 51, 68, 23, 58, 33.6, 33.2, 11, 17, 33, 53, 33, 9, 23, 33, 65, 7, 34, 25, 38, 32.7]
# lets use the list randomly generated in the previous example !

hyb = hybridize(y)
# hybridizing y to work with AMD functions

insHyb = instAvg(hyb)
# The more you use this function, the smoother is the graph

compGraph(hyb,insHyb)
```
### Resultant Graph:
![instavg](https://github.com/SayadPervez/Arduino_Master_Delta/blob/master/instavg.jpeg?raw=true)
___
___
![Mr_Handsome](https://github.com/SayadPervez/AMD-SEPERATE-DOCUMENTATION/blob/master/IMG_20190225_150001_460.jpg?raw=true)
### Sayad Pervez - the solo developer of AMD Module !
### E-Mail : [pervez2504@gmail.com](pervez2504@gmail.com)
___
___
