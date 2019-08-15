# AMD - Arduino Matplotlib DataScience
## DataScience_Function: hybridize()
___
___
# Introduction to hybrids
#### hybrid is used to pack both X and Y values of a plot together for easier accessing of functions. A hybrid is basically a tuple of two lists with the first one containing the X values (index) and the second one containing the Y values (amplitude). They have a significant advantage over the limitation offered by Dictionaries. In this Delta version, the first parameter of most of the data science functions is a hybrid. The functions discussed before this section returns only a list whereas most of the upcoming functions returns hybrids.
```python
# X and Y are lists
X = [ 1,2,3,4,5,6,7,8,9,10 ]
Y = [ 10,9,8,7,6,1,4,3,2,-5 ]

# hyb is a tuple which we refer to as an hybrid.
hyb = ( [ 1,2,3,4,5,6,7,8,9,10 ] , [ 10,9,8,7,6,1,4,3,2,-5 ] )

# Method 1:
anyFunction( x=X , y=Y )

# Method 2:
anyFunction( hyb ) # Since for most of the data science functions, the first parameter is a hybrid,
# it can be passed directly !

# It is evident that Method 2 is less time consuming than Method 1
```
___
# hybridize:-       **`Returns a hybrid`**
#### **`hybridize`** takes one or two lists as parameters and returns an hybrid.
#### **`hybridize ( li1 , li2 = None )`** is the function header.
#### When only one list is passed, the first parameter corresponds to Y-values (amplitude). When two lists are passed, the first list corresponds to X-values (index) and the second list corresponds to Y-values (amplitude).
```python
# X and Y are lists
X = [ 1,2,3,4,5,6,7,8,9,10 ]
Y = [ 10,9,8,7,6,1,4,3,2,-5 ]

hyb = hybridize( X , Y )
print(hyb)

# This would print -> ( [ 1,2,3,4,5,6,7,8,9,10 ] , [ 10,9,8,7,6,1,4,3,2,-5 ] )
```
#### When we don't need custom X values, passing just amplitude is enough. In this case X values will be automatically generated from 0 to ((length of amplitude list) - 1 )
```python
# X and Y are lists
X = [ 1,2,3,4,5,6,7,8,9,10 ]
Y = [ 10,9,8,7,6,1,4,3,2,-5 ]

hyb = hybridize( Y )
print(hyb)

# This would print -> ( [ 0,1,2,3,4,5,6,7,8,9 ] , [ 10,9,8,7,6,1,4,3,2,-5 ] )
```
> **Note:** Passing parameters with parameter names is not encouraged ! (i.e.) hyb = hybridize( li2 = Y) would throw an error.
___
### Separating a hybrid into its constituent lists:
```python
hyb = ( [ 1,2,3,4,5,6,7,8,9,10 ] , [ 10,9,8,7,6,1,4,3,2,-5 ] )

listX , listY = hyb
print(listX)
print(listY)
# This would print the following
# [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
# [10, 9, 8, 7, 6, 1, 4, 3, 2, -5]
```
___
___
![Mr_Handsome](https://github.com/SayadPervez/AMD-SEPERATE-DOCUMENTATION/blob/master/IMG_20190225_150001_460.jpg?raw=true)
### Sayad Pervez - the solo developer of AMD Module !
### E-Mail : [pervez2504@gmail.com](pervez2504@gmail.com)
___
___
