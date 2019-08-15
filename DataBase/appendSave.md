# AMD - Arduino Matplotlib DataScience
## AMD CDB Function: appendSave()
___
___
# appendSave():- **`Returns Nothing. Saves your data.`**
#### Adds a hybrid to a pre-existing AMD CDB file. The previous contents aren't deleted.
#### **`appendSave(hybrid,name,path='default')`** is the function header.
#### **`hybrid`** parameter takes the hybrid to be saved.
#### **`name`** parameter takes a string. Pass the name of the pre-existing file you want this AMD CDB to be saved at.
#### **`path`** is an optional parameter. You can give the path of the folder it needs to be saved else it is saved in the same directory as your program.
___
### Eg:
#### Currently the programs run in Trial13 python file
```python
from AMD import *
from random import randint as ri

y = [ri(0,100) for _ in range(15)]
hyb = hybridize(y)

rewriteSave(hyb,'AMD_0')
```
___
## Result:
#### Before the program was executed, the contents that already existed is displayed in the first pic.
![ghghfhgsgdfngd](https://github.com/SayadPervez/Arduino_Master_Delta/blob/master/eg4.1.JPG?raw=true)
___
#### The below pic represents the same file after execution of the program.
![hhfgdgdhfdrst](https://github.com/SayadPervez/Arduino_Master_Delta/blob/master/eg4.2.JPG?raw=true)
___
___
![Mr_Handsome](https://github.com/SayadPervez/AMD-SEPERATE-DOCUMENTATION/blob/master/IMG_20190225_150001_460.jpg?raw=true)
### Sayad Pervez - the solo developer of AMD Module !
### E-Mail : [pervez2504@gmail.com](pervez2504@gmail.com)
___
___
