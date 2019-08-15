# AMD - Arduino Matplotlib DataScience
## DataScience_Function: filter()
___
___
# filter:-       **`Returns a hybrid`**
#### filter function is used to remove unnecessary data from a list.**_This function is compatible with lists and hybrids._**.This function returns a hybrid !
#### **`filter( hybrid= None, index= [], data= [], expected= [], expectedType= None, maxDeviation= None, minDeviation= None, closeTo= None, farFrom= None, numeric= True, limit= [], frequentAverage= False, above= None, below= None )`** is the function header.
| Parameters   | Usage   |
|--------------|---------|
| hybrid = None | Pass an hybrid|
|index = []|This parameter accepts a list of X-axis values.|
| data = []| This parameter accepts a list of Y-axis values. |
| expected = [ ] | Pass a list of expected elements that you need in the filtered list |
| expectedType = [ ] | Filters data based on the type. You can pass the following as arguements : int , float , str , 'num' , 'all'. Note that **num** and **all** alone are placed within single quotes since they are custom made types. 'num' denotes all numeric data like int and float. 'all' denotes all kinds of data. When expectedType is used, numeric is set to False|
|maxDeviation = None| Permitted maximum deviation from calculated average. |
|minDeviation=None|Permitted minimum deviation from calculated average or **`farFrom`** parameter.|
|closeTo = None| Used to find data close to the given arguement. If closeTo alone is used without max_deviation, then max_deviation is taken as 1 by default. |
|farFrom=None| Pass an **numeric value** or **'avg' (string)**. if farFrom!='avg', data **`minDeviation`** units farther from the farFrom parameter is considered.      If farFrom=='avg', data **`minDeviation`** units away from average is considered.If minDeviation is not passed, minDeviation is taken as 1.  |
|numeric = True| Used to specify if you are looking for numeric data for calculation. If you wish to have strings of data in your filtered list make sure you set numeric to False. numeric = True converts all values to float and that's the reason why when expectedType is used, numeric is set to False. |
|limit = [ ]| Used to specify filter out garbage values! It basically means, no matter what, the data would not have gone beyond these limits. If it did, it is a Garbage Value. The format is **_limit=[ start-limit , end-limit ]_** |
|frequentAverage = False|Used to specify if to use most frequent data as average|
|above = None | Used to filter data above the specified value |
|below = None | Used to filter data below the specified value |

___
### Why and How average is calculated ?
#### While filtering data with max_deviation, a value has to be specified from which the upper and lower limits containing data are filter.(i.e.) if max_deviation is 1.5, data is filtered such that only data within +(or)- 1.5 than average is present in the filtered data.
### This is how average is calculated.
#### If closeTo value is present, closeTo is taken as average.
#### If closeTo value is not passed, the most frequent data piece in the list of data is taken as average.
#### If closeTo is not passed as well as all the elements in the given data are unique, average is calculated in the conventional way. But with huge garbage values, the average would shift so much that no data remains in that area returning an empty list. For that when limit parameter is passed, garbage values are filtered out earlier before other calculations take place.
___
## Depending on the number of lines you need to read, time you need to wait will increase !!!
## Garbage values occur when your arduino's pins come in contact with each other. No matter if it is a cloth or your hand, arduino is sensitive enough to sense it and give you garbage values !!
___
___
![Mr_Handsome](https://github.com/SayadPervez/AMD-SEPERATE-DOCUMENTATION/blob/master/IMG_20190225_150001_460.jpg?raw=true)
### Sayad Pervez - the solo developer of AMD Module !
### E-Mail : [pervez2504@gmail.com](pervez2504@gmail.com)
___
___
