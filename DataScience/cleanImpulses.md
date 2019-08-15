# AMD - Arduino Matplotlib DataScience
## DataScience_Function: cleanImpulses()
___
___
# cleanImpulses() **`Returns a Hybrid`**
#### This function is used to clear out multiple levels of impulses !
#### **`cleanImpulses( hyb, levels=None )`** is the function header.
#### levels parameter takes the number of times the remImp function has to be executed to give an almost flat impulse less data. level 0 represents the original data.
#### If levels parameter is not passed, it filters out all impulses until it is a flat line or a point !
## Eg:
```python
from AMD import *

y = [33, 32, 64, 67, 4, 34, 32, 47, 33.5, 26, 32, 46, 34, 51, 68, 23, 58, 33.6, 33.2, 11, 17, 33, 53, 33, 9, 23, 33, 65, 7, 34, 25, 38, 32.7]
# lets use the list randomly generated in the previous example !

hyb = hybridize(y)
# hybridizing y to work with AMD functions

flatData0 = cleanImpulses(hyb,0)
flatData1 = cleanImpulses(hyb,1)
flatData2 = cleanImpulses(hyb,2)
flatDataNone = cleanImpulses(hyb)
compGraph(hyb,flatData0)
compGraph(hyb,flatData1)
compGraph(hyb,flatData2)
compGraph(hyb,flatDataNone)
```
### Resulting Graphs:
![cleanData1](https://github.com/SayadPervez/Arduino_Master_Delta/blob/master/hyb%20vs%20level1.JPG?raw=true)
![cleanData2](https://github.com/SayadPervez/Arduino_Master_Delta/blob/master/level2%20vs%20level3.JPG?raw=true)
___
___
![Mr_Handsome](https://github.com/SayadPervez/AMD-SEPERATE-DOCUMENTATION/blob/master/IMG_20190225_150001_460.jpg?raw=true)
### Sayad Pervez - the solo developer of AMD Module !
### E-Mail : [pervez2504@gmail.com](pervez2504@gmail.com)
___
___
