# AMD - Arduino Matplotlib DataScience
## Arduino_Extraction_Function: ardata()
___
___
# ardata():-       **`Returns a list`**
#### ardata function is used to communicate with the arduino via Serial. This function returns a list of values available in the Serial port.
#### **`ardata(COM ,lines= 50 ,baudrate= 9600 ,timeout= 1 ,squeeze= True ,dynamic= False ,msg= 'a' ,dynamicDelay= 0.5, numeric= True )`** is the function header.
___
## COM
#### **`COM`** parameter is used to specify the COM port to which arduino is connected to. You can pass either an integer or a string specifying the COM port.
### Eg:
```python
# COM parameter usage:
data = ardata(8) # or
data = ardata('COM=8')
#This will be interpreted as COM8
# If your COM port's name is not in this format, use the following:
data = ardata("YOUR_COM_PORT_NAME") #or
data = ardata('COM=YOUR_COM_PORT_NAME')
```
___
## lines
#### **`lines`** denotes the number of data units or lines it reads from the Serial monitor of Arduino. The default value is set to **50** which can be changed. Note that based on another parameter **`squeeze`**, the number of elements in the list this function returns might be lesser than the that of actual data.
___
## baudrate
#### **`baudrate`** parameter is used to specify the baudrate at which the Serial communication occurs at. The default value is **9600** which is the most widely used baudrate.
___
## timeout
#### **`timeout`** is used to specify the timeout value in seconds. The default value is **1**.
___
## squeeze
#### **`squeeze`** is used to specify if the data needs to be compressed. This uses a function from data science part of this module **`compress()`** which is used to remove **_repeated and sequential_** set of data with a single piece of data.
### Eg:
```python
# Consider the following list of data:
data = [ 1 , 2 , 2 , 2 , 3 , 3 , 5 , 1 , 1 , 2 , 5 , 5 ]
info = compress(data)
print(info)
# This will print [ 1 , 2 , 3 , 5 , 1 , 2 , 5 ]
```
#### **`squeeze`** uses the same function and takes either True (or) False boolean values as parameters. By default, this parameter is set to **True**. Referencing the above example code, if squeeze is set to **False**, ardata will return **data** and if it is set to **True** which is the default setting, it will return **info**.
___
## dynamic
#### **`dynamic`** is used to specify if the Serial communication is just to read from the serial port or for both reading and writing to the serial port. The default value is **false** which means you can only read from the Serial port. If dynamic is set to true, the string from the **`msg`** parameter will be written to the Serial port every time before reading a value.
___
## msg
#### **`msg`** parameter specifies the message that is to be written in the serial monitor. the default value is **'a'**. *It is a must to pas this parameter if dynamic is set to true.*
___
## dynamicDelay
#### **`dynamicDelay`** is used to specify the time this program has to wait after writing a value to the console and to start reading from the COM port. It is experimentally determined that a delay of 0.5 seconds is mandatory in order to prevent overlapping of passed messages.
___
> Note: ardata() reads one line at a time and hence Serial.println() should be used while coding Arduino and make sure there are no unnecessary Serial.print() or Serial.println() statements present in the code.
___
## numeric
#### **`numeric`** is used to specify if the data you are expecting is of numeric type or not.
___
### Demo:
### 1) One way communication: With dynamic set to False
```C
//       Code uploaded to Arduino
int check = 2;
void setup() {
Serial.begin(9600);
pinMode(check,INPUT);
}

void loop() {
if(digitalRead(check)==HIGH)
  Serial.println("HIGH");
else
  Serial.println("LOW");
delay(500);
}
```
```python
# Python code:
from Arduino_Master import *
# info contains complete data
info = ardata(8,squeeze=False,numeric= False)
print(f"{len(info)}=>{info}")
#compressed info contains compresses form of data
CompressedInfo = compress(info)
print(f"{len(CompressedInfo)}=>{CompressedInfo}")

'''
Output:
50=>['LOW', 'LOW', 'LOW', 'LOW', 'LOW', 'LOW', 'HIGH', 'HIGH', 'HIGH', 'HIGH', 'HIGH', 'HIGH', 'HIGH', 'HIGH', 'HIGH', 'HIGH', 'HIGH', 'LOW', 'LOW', 'HIGH', 'HIGH', 'HIGH', 'HIGH', 'HIGH', 'HIGH', 'LOW', 'LOW', 'LOW', 'LOW', 'LOW', 'LOW', 'LOW', 'LOW', 'LOW', 'LOW', 'LOW', 'LOW', 'LOW', 'LOW', 'LOW', 'LOW', 'LOW', 'LOW', 'LOW', 'LOW', 'LOW', 'LOW', 'LOW', 'LOW', 'LOW']
5=>['LOW', 'HIGH', 'LOW', 'HIGH', 'LOW']

Thus actual data contains 50 elements whereas compresses data contains only 5 elements yet represents the outline of the data.
if info = ardata(8) was used instead, we would get the compressed version of data here represented by CompressedInfo.
'''
```
___
### 2) Two way communication: With dynamic set to True
```Code
//       Code uploaded to Arduino
int check = 2;
void setup() {
Serial.begin(9600);
pinMode(check,INPUT);
}

void loop() {
if(Serial.available()>0)
{
  if(Serial.readString()=="State")
  {
          if(digitalRead(check)==HIGH)
            Serial.println("HIGH");
          else
            Serial.println("LOW");
  }

delay(500);
}
}
// This code will print the result on the serial monitor only if "State" is sent to the serial monitor
```
```python
#   Python code
from Arduino_Master import *

info = ardata(8,dynamic=True,msg="State",numeric=False)
print(info)
'''
This would print
['LOW', 'HIGH', 'LOW', 'HIGH', 'LOW', 'HIGH']
Since squeeze by default is set to True, data is compressed!
'''
```
### Though both these demonstrations are used to extract data from Arduino, the later is better than the former. The reason is that when dynamic is set to True, we ask for instantaneous information whereas when dynamic is set to False, there is a possibility of getting initial data alone rather than instantaneous data since arduino keeps writing the values to the Serial monitor.
### The functionality being inherited from pyserial, It is possible to call all functions from pyserial module without prefixing the functions with 'serial.' statement.
___
___
