# AMD - Arduino Matplotlib DataScience
## Arduino_Extraction_Function: dynamicSerial()
___
___
# dynamicSerial:-        **`Returns a list with only one element`**
#### **`dynamicSerial`** is similar to dynamic mode of ardata() except that this returns a **_list_** with just one element in it.
#### **`dynamicSerial( COM , baudrate = 9600 , timeout = 1 , msg = "a" , dynamicDelay = 0.5 )`** is the function header.
| Parameters | Usage |
|------------|------|
| COM        | Specify the COM port. Similar to ardata(), you can pass either an integer or the complete name as a string.|
| baudrate =9600| Set the baudrate. Default value is **9600**. |
| timeout =1| Set the timeout. Default is **1**|
| msg ="a"| String to be written to the Serial Port |
| dynamicDelay = 0.5| Similar to that of ardata's dynamicDelay. Default value is set to **0.5 seconds**. Any value lesser than this would result in overlapping of the input. |

#### This function returns a list with only one element.
___
### Note:
#### For an arduino program that prints a value on Serial monitor only when we send it a value, the combination of writeSerial and readSerial functions won't work. dynamicSerial has to be used at that place.
```python
# Use
dynamicSerial(8,msg="Give DATA")

# INSTEAD OF
writeSerial(8,msg="Give Data")
data=readSerial(8)

# The latter would only return an empty list !!!
```
___
___
![Mr_Handsome](https://github.com/SayadPervez/AMD-SEPERATE-DOCUMENTATION/blob/master/IMG_20190225_150001_460.jpg?raw=true)
### Sayad Pervez - the solo developer of AMD Module !
### E-Mail : [pervez2504@gmail.com](pervez2504@gmail.com)
___
___
