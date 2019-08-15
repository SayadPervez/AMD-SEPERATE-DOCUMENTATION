# AMD - Arduino Matplotlib DataScience
## DataScience_Function: compGraph()
___
___
# compGraph:-       **`Returns Nothing. Just plots a Graph`**
#### **`compGraph`** is used to compare two sets of data (any combination of list, dictionary or a hybrid)
#### **`compGraph( hybrid1= None, hybrid2 =None, x1= [], y1= [], x2= [], y2= [], xlabel= 'dataPiece', ylabel= 'Amplitude', label1= 'myData-1', label2= 'myData-2', color1= 'red', color2= 'blue', title= 'Graph', markersize= 7, stl= 'dark_background', fit= True, d1= {}, d2= {} )`** is the function header.
| Parameters   | Usage   |
|--------------|---------|
|hybrid1 = None| pass first hybrid |
|hybrid2 = None| pass second hybrid |
| x1 = []|Pass a list of values to be plotted along X-axis for the first plot.|
| y1 = []     | Pass a list of values to be plotted along the y-axis. The x-axis is automatically generated depending on the number of parameters in your given list if x1 is not passed.|
| x2 = []|Pass a list of values to be plotted along X-axis for the second plot.|
| y2 = []     | Pass a list of values to be plotted along the y-axis. The x-axis is automatically generated depending on the number of parameters in your given list if x2 is not passed.|
| xlabel = 'dataPiece' | Used to label the X-axis legend |
| ylabel = 'Amplitude' | Used to label the Y-axis legend |
| label1 = 'myData-1' | What you want your first set data to be called |
| label2 = 'myData-2' | What you want your second set data to be called |
| color1 = 'red' | What color you want your first set of data to be plotted with |
| color2 = 'blue' | What color you want your second set of data to be plotted with |
| title = 'Graph' | Name of the graph |
| markersize = 7| Size of the plotting line. |
| stl = 'dark_background' | Style of Graph you wish. Refer this StyleSheet => [StyleSheet](https://matplotlib.org/3.1.0/gallery/style_sheets/style_sheets_reference.html) |
| d1 = {} | Used to pass a dictionary as the first set of data. This is used only when you need custom x values instead of default sequentially arranged X-values. y and d1 must not be passed together. |
| d2 = {} | Used to pass a dictionary as the second set of data. This is used only when you need custom x values instead of default sequentially arranged X-values. y2 and d2 must not be passed together. |
| fit = True | A bit complex, and hence explained below |
| equiAxis = False | To specify whether the axes units should be exact. [Learn More here](https://github.com/SayadPervez/Arduino_Master_Delta/blob/master/equiaxis.md)|

___
## fit
#### **`fit`** parameter is used to specify if both the graphs need to be scaled to the maximum size or not. When y and y2 values have different number of elements **`fit = True`** enables changing X-values of the list of data which has less number of elements to equalize and approximate the correctness of distribution of data.
## When using lists:
```python
# Code for left graph
y1=[11,12.7,13,14,15,12.3,11.4,13,12.5,12.4,12.3,12.4,10,9]
y2=[12.7,13,12.3,12.7,12.4,12.3,12.4]
compGraph(y1=y1,y2=y2,fit= False)

# Code for right graph
y1=[11,12.7,13,14,15,12.3,11.4,13,12.5,12.4,12.3,12.4,10,9]
y2=[12.7,13,12.3,12.7,12.4,12.3,12.4]
compGraph(y1=y1,y2=y2)
```
### With Fit **Disabled (left)** and With Fit **Enabled (right)**
![Fit](https://github.com/SayadPervez/Arduino_Master_Delta/blob/master/Fit%20lists.JPG?raw=true)
___
## When using hybrids:
```python
y1=[11,12.7,13,14,15,12.3,11.4,13,12.5,12.4,12.3,12.4,10,9]
y2=[12.7,13,12.3,13,12.5,12.4,12.3,12.4]
x2=[1,2,5,7,8,9,10,11]    # x2 values were created based on the position of y2 elements in y1.
# Filter function would ease this process !
# Which will be explained soon !!

hyb1 = hybridize(y1) # x1 values are automatically generated !
hyb2 = hybridize(x2,y2) # x2 values are provided

compGraph(hyb1,hyb2) # fit is set to False
```
### Since when hybrids are used, Fit is disabled for accuracy !
![Fit hybrid](https://github.com/SayadPervez/Arduino_Master_Delta/blob/master/Fit%20hybrids.jpeg?raw=true)
#### In the above pics, the red colored data represents raw_data and blue colored data represents filtered data. So naturally filtered set of data will have less number of elements in it and if compGraph() function is used the result would be similar to the left Graph which looks a bit absurd. When **fit = True** enables data to fit into the whole graph without affecting the Amplitude of the data. In simple words, smaller list of data is stretched to the size of the bigger list of data along the X-axis to give an **_approximation_** without using dictionaries which are comparatively difficult to use than lists so as to make the functions newbie friendly.
#### **_Fit is set to False when hybrids are used._**
#### compGraph is similar to Graph function just with visualizing one more list of data
___
___
![Mr_Handsome](https://github.com/SayadPervez/AMD-SEPERATE-DOCUMENTATION/blob/master/IMG_20190225_150001_460.jpg?raw=true)
### Sayad Pervez - the solo developer of AMD Module !
### E-Mail : [pervez2504@gmail.com](pervez2504@gmail.com)
___
___
