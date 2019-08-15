# Projects that can be done with Arduino:
___
___
# Demo:
# Garbage Value Removal:
```C
String msg;
const int trigPin = 9;
const int echoPin = 10;
double duration;
float distance;

void setup()
{
    Serial.begin(9600);
    pinMode(echoPin, INPUT);
    pinMode(trigPin, OUTPUT);
}

void loop()
// If information is available in Serial port from arduino get it and then checking for the distance
{   if (Serial.available()>0)
{
    msg=Serial.readString() ;
    if(msg=="d")
      {
        digitalWrite(trigPin, LOW);
        delayMicroseconds(2);
        digitalWrite(trigPin, HIGH);
        delayMicroseconds(10);
        digitalWrite(trigPin, LOW);
        duration = pulseIn(echoPin, HIGH);
        distance= duration/29/2;
        Serial.println(distance);
       }
    else
      int i=0; // Just Do nothing.....(Never Mind statement !!! )

}
}
```
___
```Python
# importing area !!
from AMD import *

# collecting data and saving it as a list in rawData
rawData = ardata(7,lines=50,dynamic=True,msg='d')  # if set is not used, the most repeated set of value would be taken as average !

# Inserting garbage values for checking,
rawData.insert(13,600)
rawData.insert(28,5600)

# rawHybrid contains hybridized form of rawData
rawHybrid = hybridize( rawData )
print(rawHybrid)
filteredHybrid = filter(rawHybrid,expectedType='num',limit=[0,200],maxDeviation=10)
print("")
print(filteredHybrid)

Graph(hybridize(rawData))
Graph(filteredHybrid)
compGraph(rawHybrid,filteredHybrid)
```
___
![Garbage_Value_removal_1](https://github.com/SayadPervez/Arduino_Master_Delta/blob/master/___1___.jpeg?raw=true)
### Without any filter, The above pic displays the data from Arduino with custom added garbage values in order to test.
___
![Garbage_Value_removal_2](https://github.com/SayadPervez/Arduino_Master_Delta/blob/master/___2___.jpeg?raw=true)
### Data after filtering is displayed above !! Thus conventional average works fine !!
___
![Garbage_Value_removal_3](https://github.com/SayadPervez/Arduino_Master_Delta/blob/master/___3___.jpeg?raw=true)
### Comparison of data is displayed above. Since the limits of the sensor were specified, values as high as 4500 and 6000 were removed and then the average was calculated making this module a well built one. Red is raw data whereas Blue is filtered data.
___
## If used correctly, you can filter your data in the following ways !!!
![Example_1](https://github.com/SayadPervez/Arduino_Master_Delta/blob/master/Light%20Intensity.jpeg?raw=true)
### Check light intensity and with previously measured values, you can check if the light is switched on or not just using an LDR.
### Arduino Code:
```C
int ldr = A0;
void setup() {
Serial.begin(9600);
pinMode(ldr,INPUT);
}

void loop() {
if(Serial.available()>0)
{
  if(Serial.readString()=="d")
  {
          Serial.println(analogRead(ldr)*5.0/1023.0);
  }

}
}
```

### Python Code:
``` Python
rawData = ardata(7,lines=50,dynamic=True,msg='d')  # if set is not used, the most repeated set of value would be taken as average !

# rawHybrid contains hybridized form of rawData
rawHybrid = hybridize( rawData )
print(rawHybrid)
Hybrid = filter(rawHybrid,expectedType='num',limit=[0,3.5]) # Just filtering out garbage values if any
print("")
print(Hybrid)

ind , data = Hybrid # Seperating the hybrid

#Segregating Data:
newData=[]
for z in range(len(data)):
    if (data[z]>1.5):
        newData.append("Light On")
    else:
        newData.append("It's Dark")
filteredHybrid = hybridize(ind , newData)


compGraph(Hybrid,filteredHybrid)
```
___
___
![Example_2](https://github.com/SayadPervez/Arduino_Master_Delta/blob/master/Impulse%20Removal%203.jpeg?raw=true)
###  Impulse removal Example in the above pic
### Arduino_Code:
```C
String msg;
const int trigPin = 9;
const int echoPin = 10;
double duration;
float distance;

void setup()
{
    Serial.begin(9600);
    pinMode(echoPin, INPUT);
    pinMode(trigPin, OUTPUT);
}

void loop()
// If information is available in Serial port from arduino get it and then checking for the distance
{   if (Serial.available()>0)
{
    msg=Serial.readString() ;
    if(msg=="d")
      {
        digitalWrite(trigPin, LOW);
        delayMicroseconds(2);
        digitalWrite(trigPin, HIGH);
        delayMicroseconds(10);
        digitalWrite(trigPin, LOW);
        duration = pulseIn(echoPin, HIGH);
        distance= duration/29/2;
        Serial.println(distance);
       }
    else
      int i=0; // Just Do nothing.....(Never Mind statement !!! )

}
}
```
### Python Code for impulse removal:
```python
# collecting data and saving it as a list in rawData
rawData = ardata(7,lines=50,dynamic=True,msg='d')  # if set is not used, the most repeated set of value would be taken as average !

# rawHybrid contains hybridized form of rawData
rawHybrid = hybridize( rawData )
print(rawHybrid)
filteredHybrid = filter(rawHybrid,expectedType='num',limit=[0,200],maxDeviation=5,frequentAverage=True)
print("")
print(filteredHybrid)

Graph(hybridize(rawData))
Graph(filteredHybrid)
compGraph(rawHybrid,filteredHybrid)
```
___
___
![Example_3](https://github.com/SayadPervez/Arduino_Master_Delta/blob/master/Impulse%20Detection.png?raw=true)
### You can also detect and measure impulses !!!
### Arduino Code is same as the above one ! Python code for impulse detection and measurement is :
```python
# collecting data and saving it as a list in rawData
rawData = ardata(7,lines=50,dynamic=True,msg='d')  # if set is not used, the most repeated set of value would be taken as average !

# rawHybrid contains hybridized form of rawData
rawHybrid = hybridize( rawData )
print(rawHybrid)
filteredHybrid = filter(rawHybrid,expectedType='num',limit=[0,200],maxDeviation=7,closeTo=20) # since  I know impulse are going to be near 20 cm from the ultrasonic sensor !
print("")
print(filteredHybrid)

Graph(hybridize(rawData))
Graph(filteredHybrid)
compGraph(rawHybrid,filteredHybrid)
```
___
___
![Mr_Handsome](https://github.com/SayadPervez/AMD-SEPERATE-DOCUMENTATION/blob/master/IMG_20190225_150001_460.jpg?raw=true)
### Sayad Pervez - the solo developer of AMD Module !
### E-Mail : [pervez2504@gmail.com](pervez2504@gmail.com)
___
___
