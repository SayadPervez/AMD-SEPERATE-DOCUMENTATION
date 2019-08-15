# AMD - Arduino Matplotlib DataScience
## AMD CDB Function: save()
___
___
# save():- **`Returns Nothing. Saves your data.`**
#### Saves a hybrid as a AMD CDB file.
#### **`save(hybrid,name='default',path='default')`** is the function header.
#### **`hybrid`** parameter takes the hybrid to be saved.
#### **`name`** parameter takes a string. Pass the name you want this AMD CDB to be saved as. If no name is passed, AMD_(a sequential number) is set as the name. If the file with specified name already exists, It saves the contents in another file as AMD_Cache File.
#### **`path`** is an optional parameter. You can give the path of the folder it needs to be saved else it is saved in the same directory as your program.
___
### Eg:
#### Currently the programs run in Trial13 python file
```python
from AMD import *
from random import randint as ri

y = [ri(0,100) for _ in range(100)]
hyb = hybridize(y)

save(hyb,'AMD CDB 0')
```
## Result:
![eg1.1](https://github.com/SayadPervez/Arduino_Master_Delta/blob/master/eg1.1.JPG?raw=true)
___
```python
from AMD import *
from random import randint as ri

y = [ri(0,100) for _ in range(100)]
hyb = hybridize(y)

save(hyb) # saved as AMD_0
save(hyb) # saved as AMD_1
# saved in the same directory as the file.
```
## Result:
![eg2.1](https://github.com/SayadPervez/Arduino_Master_Delta/blob/master/eg2.1.JPG?raw=true)
___
```python
from AMD import *
from random import randint as ri

y = [ri(0,100) for _ in range(100)]
hyb = hybridize(y)

save(hyb,'AMD Path Eg','P:\\Pvz_Program_Files\\Other programs\\Trail AMD CDB')
# saved as 'AMD Path Eg' in the specified directory
# you can also use
# save(hyb,'P:\\Pvz_Program_Files\\Other programs\\Trail AMD CDB\\AMD Path Eg')
```
## Result:
![eg3.1](https://github.com/SayadPervez/Arduino_Master_Delta/blob/master/eg3.1.JPG?raw=true)
___
___
![Mr_Handsome](https://github.com/SayadPervez/AMD-SEPERATE-DOCUMENTATION/blob/master/IMG_20190225_150001_460.jpg?raw=true)
### Sayad Pervez - the solo developer of AMD Module !
### E-Mail : [pervez2504@gmail.com](pervez2504@gmail.com)
___
___
