# AMD - Arduino Matplotlib DataScience
## AMD CDB Function: extractY()
___
___
# extractY():- **`Returns Hybrid.`**
#### extracts Y values from a AMD CDB.
#### **`extractY(name,path=None)`** is the function header.
#### **`name`** parameter takes a string. Pass the name of the pre-existing AMD CDB file you want to extract Data from.
#### **`path`** is an optional parameter. You can give the path of the folder of the pre-existing AMD CDB file.
___
### Eg:
```python
from AMD import *

from random import randint as ri

y=extractY('AMD_0') # in same folder as the program.
# else give the absoulte address !

print(y)

# This would print [86.0, 91.0, 50.0, 83.0, 83.0, 66.0, 97.0, 7.0, 2.0, 75.0, 60.0, 36.0, 97.0, 61.0, 50.0]
```

___
___
![Mr_Handsome](https://github.com/SayadPervez/AMD-SEPERATE-DOCUMENTATION/blob/master/IMG_20190225_150001_460.jpg?raw=true)
### Sayad Pervez - the solo developer of AMD Module !
### E-Mail : [pervez2504@gmail.com](pervez2504@gmail.com)
___
___
