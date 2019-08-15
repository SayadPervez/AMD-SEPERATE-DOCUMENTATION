# AMD - Arduino Matplotlib DataScience
## DataScience_Function: reduce()
___
___
# reduce():- **`Returns a Hybrid`**
#### **`reduce(hyb)`** is the fucntion header.
#### This function takes the first two points and creates a point whose x and y co-ordinates are the average of x and y values of the first two points themselves. When repeated, they reduce the x co-ordinates one by one and yet give an approximation of data trend.
## Eg:
```python
from AMD import *

y = [33, 32, 64, 67, 4, 34, 32, 47, 33.5, 26, 32, 46, 34, 51, 68, 23, 58, 33.6, 33.2, 11, 17, 33, 53, 33, 9, 23, 33, 65, 7, 34, 25, 38, 32.7]
# lets use the list randomly generated in the previous example !

hyb = hybridize(y)
# hybridizing y to work with AMD functions
red = hyb
for _ in range(7):
    red = reduce(red)

compGraph(hyb,red)
```
### Resulting Graph:
![reduce](https://github.com/SayadPervez/Arduino_Master_Delta/blob/master/Reduce.jpeg?raw=true)
___
___
![Mr_Handsome](https://github.com/SayadPervez/AMD-SEPERATE-DOCUMENTATION/blob/master/IMG_20190225_150001_460.jpg?raw=true)
### Sayad Pervez - the solo developer of AMD Module !
### E-Mail : [pervez2504@gmail.com](pervez2504@gmail.com)
___
___
