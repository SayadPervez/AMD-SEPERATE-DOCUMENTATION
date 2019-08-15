# AMD - Arduino Matplotlib DataScience
## Arduino_Extraction_Function: readSerial()
___
___
# readSerial:-       **`Returns a value( int / float / String )`**
#### **`readSerial`** reads only one line from the Arduino.
#### **`readSerial( COM , baudrate = 9600 , timeout = 1 )`** is the function header.
| Parameters | Usage |
|------------|------|
| COM        | Specify the COM port. Similar to ardata(), you can pass either an integer or the complete name as a string.|
| baudrate =9600| Set the baudrate. Default value is **9600**. |
| timeout =1| Set the timeout. Default is **1**|

#### returns a element (if available within timeout !). numeric is set to False for readSerial.
___
___
