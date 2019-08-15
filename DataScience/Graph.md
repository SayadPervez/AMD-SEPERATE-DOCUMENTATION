# AMD - Arduino Matplotlib DataScience
## DataScience_Function: Graph()
___
___
# Graph:-       **`Returns Nothing. Just plots a Graph`**
#### **`Graph`** function is used to visualize a list of data.
#### **`Graph( hybrid= None, x= [], y= [], xlabel= 'dataPiece', ylabel= 'Amplitude', label= 'myData', color= 'red', title= 'Graph', markersize= 7, stl= 'dark_background', d= {}, mark= 'x' ,equiAxis=False)`** is the function header.
| Parameters   | Usage   |
|--------------|---------|
| hybrid = None | Used to pass a hybrid. Since it si the first parameter, hybrid can be passed directly without the parameter name |
| x = [] | Pass a list of valuesto be plotted along the x-axis. |
| y = []     | Pass a list of values to be plotted along the y-axis. The x-axis is automatically generated depending on the number of parameters in your given list if no **`hybrid`** or **`x`** parameter is passed.|
| xlabel = 'dataPiece' | Used to label the X-axis legend |
| ylabel = 'Amplitude' | Used to label the Y-axis legend |
| label = 'myData' | What you want your data to be called |
| color = 'red' | What color you want your data to be plotted with |
| title = 'Graph' | Name of the graph |
| mark = 'x' | Used to set the marker type. Refer this StyleSheet => [Marker_Style_Sheet](https://matplotlib.org/3.1.0/api/markers_api.html) |
| markersize = 7| Size of the plotting line. |
| stl = 'dark_background' | Style of Graph you wish. Refer this StyleSheet => [StyleSheet](https://matplotlib.org/3.1.0/gallery/style_sheets/style_sheets_reference.html) |
| d = {} | Used to pass a dictionary. This is used only when you need custom x values instead of default sequentially arranged X-values. y and d must not be passed together. |
| equiAxis = False | To specify whether the axes units should be exact. [Learn More here](https://github.com/SayadPervez/Arduino_Master_Delta/blob/master/equiaxis.md)|


#### Passing Strings to y (or) Dictionaries whose values are strings will also be plotted accordingly !
___
### Demo:
### Demonstration 1: Passing a list to y
```Python
# Python Code
myList = [ 1 , 2 , 3 , 4 , 5 , 1 , 7 , 7 , 10 , 8]
Graph(y = myList)
```
### Output:
![Graph_1](https://github.com/SayadPervez/Arduino_Master_Delta/blob/master/G1.jpeg?raw=true)
___
### Demonstration 2: Plotting using a dictionary to get custom X-values.
```Python
# Python Code
myDict = { 0:10 , 1:12 , 2:12.05 , 3:-0.1 , 4:-12.05 , 5:0 , 6:5 , 6:5 , 10:5.5 }
Graph(d=myDict)
```
### Output:
![Graph_2](https://github.com/SayadPervez/Arduino_Master_Delta/blob/master/G2.jpeg?raw=true)
___
### Demonstration 3: Plotting Strings:
```python
# Python code
listOfStrings = ['LOW', 'LOW', 'LOW', 'LOW', 'LOW', 'LOW', 'HIGH', 'HIGH', 'HIGH', 'HIGH', 'HIGH', 'HIGH', 'HIGH', 'HIGH', 'HIGH', 'HIGH', 'HIGH', 'LOW', 'LOW', 'HIGH', 'HIGH']
Graph(y = listOfStrings)
```
### Output:
![Graph_3](https://github.com/SayadPervez/Arduino_Master_Delta/blob/master/G3.jpeg?raw=true)
#### The same can also be done by passing a Dictionary !
___
### Demonstration 4: Using hybrid:
```python
#python code
X = [ 1 , 13 , 14 , 17 , 18 , 25 , 27 , 27 , 30 , 45 ]
Y = [ 1 , 2 , 3 , 4 , 5 , 1 , 7 , 8 , 10 , 8]

hyb = hybridize(X,Y)
Graph(hyb)

# Graph( x=X ,y=Y ) would give the same output but it is a better practice to use hybrids since key functions like filter takes and returns hybrids.
```
### Output:
![Graph_4](https://github.com/SayadPervez/Arduino_Master_Delta/blob/master/G4.jpeg?raw=true)
___
___
![Mr_Handsome](https://github.com/SayadPervez/AMD-SEPERATE-DOCUMENTATION/blob/master/IMG_20190225_150001_460.jpg?raw=true)
### Sayad Pervez - the solo developer of AMD Module !
### E-Mail : [pervez2504@gmail.com](pervez2504@gmail.com)
___
___
