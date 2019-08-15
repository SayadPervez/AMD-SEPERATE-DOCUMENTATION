# AMD - Arduino Matplotlib DataScience
## DataScience_Function: smoothie()
___
___
# smoothie():- **`Returns a Hybrid`**
#### **`smoothie( hyb , levels= None)`**
#### Similar to cleanImpulses function being a repetition tool for remImp, smoothie is a repetition function for  instAvg. level 0 represents original data and greater the levels, smoother would be the data. Not passing levels arguement would give just the final point.
## Eg:
```python
from AMD import *

y = [33, 32, 64, 67, 4, 34, 32, 47, 33.5, 26, 32, 46, 34, 51, 68, 23, 58, 33.6, 33.2, 11, 17, 33, 53, 33, 9, 23, 33, 65, 7, 34, 25, 38, 32.7]
# lets use the list randomly generated in the previous example !

hyb = hybridize(y)
# hybridizing y to work with AMD functions

sm2 = smoothie( hyb , 2)
sm15 = smoothie( hyb , 15)

compGraph(sm2,sm15)

```
### Resulting Graph:
![smoothie](https://github.com/SayadPervez/Arduino_Master_Delta/blob/master/smoothie.jpeg?raw=true)
___
___
![Mr_Handsome](https://github.com/SayadPervez/AMD-SEPERATE-DOCUMENTATION/blob/master/IMG_20190225_150001_460.jpg?raw=true)
### Sayad Pervez - the solo developer of AMD Module !
### E-Mail : [pervez2504@gmail.com](pervez2504@gmail.com)
___
___
