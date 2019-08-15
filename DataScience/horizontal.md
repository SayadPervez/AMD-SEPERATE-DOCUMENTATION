# AMD - Arduino Matplotlib DataScience
## DataScience_Function: horizontal()
___
___
# horizontal:-       **`Returns Nothing. Just a placeholder for graph`**
#### Creates a line parallel to  X-axis.
#### **`horizontal( y , lbl = 'horizontal' , start = 0 , end = 10 , stl = 'dark_background',color='yellow')`** is the function header.
|Parameter| Usage|
|---------|------|
|y|The distance from the origin is specified here|
|lbl = 'horizontal'|label is set to 'horizontal' by default|
|start = 0| value from which this line should start|
|end = 10 | value at which this line should end |
|color='yellow'|Color of the horizontal|
|stl='dark_background'|Set the style of the plot. Refer this StyleSheet => [StyleSheet](https://matplotlib.org/3.1.0/gallery/style_sheets/style_sheets_reference.html)|

#### Use this function before the Graph() function you wish the line to plotted in.
___
___
# vertical:-       **`Returns Nothing. Just a placeholder for graph`**
#### Creates a line parallel to  Y-axis.
#### **`vertical( x , lbl = 'vertical' , start = 0 , end = 10 , stl = 'dark_background',color='yellow')`** is the function header.
|Parameter| Usage|
|---------|------|
|x|The distance from the origin is specified here|
|lbl = 'vertical'|label is set to 'vertical' by default|
|start = 0| value from which this line should start|
|end = 10 | value at which this line should end |
|color='yellow'|Color of the vertical|
|stl='dark_background'|Set the style of the plot. Refer this StyleSheet => [StyleSheet](https://matplotlib.org/3.1.0/gallery/style_sheets/style_sheets_reference.html)|

#### Use this function before the Graph() function you wish the line to plotted in.
___
### vertical and horizontal are used as markers in a graph and are yellow in color by default !
```Python
vertical(6.5)
horizontal(5,start=3,end=7,color='cyan')
Graph(y=[1,2,3,4,5,6,7,8,9,10])
# This would result in the following Graph

```
![HorizonalVertical](https://github.com/SayadPervez/Arduino_Master_Delta/blob/master/VerticalHorizontal.jpeg?raw=true)
___
# marker:-       **`Returns Nothing. Just a placeholder for graph`**
#### **`marker`** function creates a plus shaped plot at a given co-ordinate.
#### **`marker( x , y , limit = 1 , lbl = "marker" , stl = 'dark_background',color='yellow')`** is the function header.
|Parameter| Usage|
|---------|------|
|x|X Coordinate|
|y|Y Coordinate|
|limit=1| size of the marker|
|lbl='marker'|specify a label|
|color='yellow'|Color of the marker|
|stl='dark_background'|Set the style of the plot. Refer this StyleSheet => [StyleSheet](https://matplotlib.org/3.1.0/gallery/style_sheets/style_sheets_reference.html)|

#### Use this function before the Graph() function you wish this marker to be plotted
```python
marker(5,6,color='green')
Graph(y=[1,2,3,4,5,6,7,8,9,10])
# This would result in the following Graph
```
![markers_2](https://github.com/SayadPervez/Arduino_Master_Delta/blob/master/Marker.jpeg?raw=true)
___
___
![Mr_Handsome](https://github.com/SayadPervez/AMD-SEPERATE-DOCUMENTATION/blob/master/IMG_20190225_150001_460.jpg?raw=true)
### Sayad Pervez - the solo developer of AMD Module !
### E-Mail : [pervez2504@gmail.com](pervez2504@gmail.com)
___
___
