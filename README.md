# Arduino_Master_Delta(AMD) Version 2.2.0
## From Version 2.2 AMD  will stand for Arduino-Matplotlib-DataScience since I've implemented various functions as in the new expansion in this single module.
![introPic](https://github.com/SayadPervez/AMD--TUTORIAL/blob/master/IntroPic.png?raw=true)
![introPic](https://github.com/SayadPervez/Arduino_Master_Delta/blob/master/Trust%20me%20both%20are%20same.JPG?raw=true)
___
# What's the difference between Alpha and Delta Versions ?
#### >>> Alpha version provides ` easier but approximate ` interface for data extraction and Visualization **_(Since X values are automatically generated and fit enables only approximation of the data plotting)_**.
#### >>> Delta version of Arduino_Master is designed to deliver `accurate visualization` and hence a bit more complex than Alpha versions.
#### >>> To ease using of functions, Delta version uses a specific type of input called `hybrid` to represent both the X and Y values of a given plot with just one variable.
#### >>> Default plotting style is 'dark_background' unlike 'ggplot' of Alpha.
#### >>> Link to Arduino_Master (Alpha Version) [Arduino_Master_Alpha](https://pypi.org/project/Arduino-Master/). Note that this module is officially not supported anymore. That is no updates would be added to it and also the availability of data science functions are less.
___
___
# What's New in 2.2.0 ?
#### >>> Bugs related to readSerial, writeSerial and dynamicSerial fixed.
#### >>> **`farFrom`** and **`minDeviation`** parameters added to **`filter`** function.
#### >>> Bugs in filter function that prevented the use of farFrom, closeTo, maxDeviation and minDeviation parameters together **_rectified_**.
#### >>> **`compress()`** function updated to work with hybrids too !! (Version-0.9.2)
#### >>> 'avg' can also be passed to **`closeTo`** parameter of the filter function !! (Version-1.2)
#### >>> **`below`** and **`above`** parameters added to filter function ! (Version-1.3)
#### >>> 9 new data science functions added !! (Version-1.4)
#### >>> hybridize function updated to check if both index and amplitude lists have equal number of elements ! (Version-1.5)
#### >>> **`equiAxis'** parameter added to Graph, compGraph and visualizeSmoothie functions !!! (Version-1.5)
#### >>> Font Bug in plotting functions **_rectified_** !!  (Version-1.6)
#### >>> The debugging of the previuos bug which I cleared out in  Version 1.6 gave some more bugs, I got it **_rectified_**. You guys know about this, You are programmers !!  (Version-1.7)
#### >>> Change 1.6 as 1.7 in my previous point.Checked it, everything is fine to go now ! (Version-1.8)  
#### >>> Included docstrings and compatibility checked with all operating systems and jupyter notebook ! (Version-2.0)
#### >>> Functions like densePop, scarcePop, remImp, detectImp, cleanImpulses, reduce, instAvg, smoothie, Graph, compGraph and visualizeSmoothie modified to work even if you pass a list at the place of a hybird. But for accurate Data visualizations I'd recommend using hybrids. However all those functions returns hybrids alone as usual. Maximum error tolerance from this version !!!!!!!!!!!!!!!!!! (Version-2.1)
#### >>> Data storage module compatibility added !! (Version-2.2.0)
#### >>> 6 New functions providing data storage and retrieval interface added !!  (Version-2.2.0)
___
___
### AMD tutorial in this link -> [tutorial](https://github.com/SayadPervez/AMD--TUTORIAL/blob/master/README.md)
___
___
# Intro:
#### Embedded C is used to program microcontrollers like Arduino. However embedded C could never compete with Python's simplicity and functionality. Also Arduino being a microcontroller, we get a lot of garbage values which we require to filter before utilizing. This module eases the process of extracting and passing data to Arduino via Serial communication.
#### This Module also provides Easy and flexible Data Science functions for Data extraction, filtering, removing garbage values and Data Visualization !
___
___
# Installing via pip:
### Use the following command to install Arduino_Master using pip.
### **`pip install AMD`**
___
___
# Automatic Installation of other required Modules:
#### This module requires two more packages namely **`pyserial`** and **`matplotlib`**. Yet just by importing this module using the import statement or by using any function, unavailable modules will be installed and imported automatically. Make sure you have good internet connection and if still you get ModuleNotFound error, try installing these two modules manually via pip.
___
___
# Importing Functions:
#### **`from AMD import *`** statement is used to import all available functions from Arduino_Master. This version contains the following functions which we'll be discussing shortly. These functions can be  grouped into 3 categories:
___
### [>> For Extracting and Writing data to Arduino:](https://github.com/SayadPervez/AMD-SEPERATE-DOCUMENTATION/blob/master/Arduino_Data_Extraction_Functions.md)
#### [$ ardata](https://github.com/SayadPervez/AMD-SEPERATE-DOCUMENTATION/blob/master/ardata().md)
#### [$ readSerial](https://github.com/SayadPervez/AMD-SEPERATE-DOCUMENTATION/blob/master/readSerial.md)
#### [$ writeSerial](https://github.com/SayadPervez/AMD-SEPERATE-DOCUMENTATION/blob/master/writeSerial.md)
#### [$ dynamicSerial](https://github.com/SayadPervez/AMD-SEPERATE-DOCUMENTATION/blob/master/dynamicSerial.md)
___
### [>> Data Science enabled functions for filtering and visualizing Data:](https://github.com/SayadPervez/AMD-SEPERATE-DOCUMENTATION/blob/master/DataScience/DataScience%20Main.md)
#### [$ hybridize](https://github.com/SayadPervez/AMD-SEPERATE-DOCUMENTATION/blob/master/DataScience/hybrids.md)
#### [$ Graph](https://github.com/SayadPervez/AMD-SEPERATE-DOCUMENTATION/blob/master/DataScience/Graph.md)
#### [$ compGraph](https://github.com/SayadPervez/AMD-SEPERATE-DOCUMENTATION/blob/master/DataScience/compGraph.md)
#### [$ horizontal](https://github.com/SayadPervez/AMD-SEPERATE-DOCUMENTATION/blob/master/DataScience/horizontal.md)
#### [$ vertical](https://github.com/SayadPervez/AMD-SEPERATE-DOCUMENTATION/blob/master/DataScience/vertical.md)
#### [$ marker](https://github.com/SayadPervez/AMD-SEPERATE-DOCUMENTATION/blob/master/DataScience/marker.md)
#### [$ most_frequent](https://github.com/SayadPervez/AMD-SEPERATE-DOCUMENTATION/blob/master/DataScience/most_frequent.md)
#### [$ least_frequent](https://github.com/SayadPervez/AMD-SEPERATE-DOCUMENTATION/blob/master/DataScience/least_frequent.md)
#### [$ compress](https://github.com/SayadPervez/AMD-SEPERATE-DOCUMENTATION/blob/master/DataScience/compress.md)
#### [$ filter](https://github.com/SayadPervez/AMD-SEPERATE-DOCUMENTATION/blob/master/DataScience/filter.md)
#### [$ densePop](https://github.com/SayadPervez/AMD-SEPERATE-DOCUMENTATION/blob/master/DataScience/densePop.md)
#### [$ scarcePop](https://github.com/SayadPervez/AMD-SEPERATE-DOCUMENTATION/blob/master/DataScience/scarcePop.md)
#### [$ remImp](https://github.com/SayadPervez/AMD-SEPERATE-DOCUMENTATION/blob/master/DataScience/remImp.md)
#### [$ detectImp](https://github.com/SayadPervez/AMD-SEPERATE-DOCUMENTATION/blob/master/DataScience/detectImp.md)
#### [$ cleanImpulses](https://github.com/SayadPervez/AMD-SEPERATE-DOCUMENTATION/blob/master/DataScience/cleanImpulses.md)
#### [$ reduce](https://github.com/SayadPervez/AMD-SEPERATE-DOCUMENTATION/blob/master/DataScience/reduce.md)
#### [$ instAvg](https://github.com/SayadPervez/AMD-SEPERATE-DOCUMENTATION/blob/master/DataScience/instAbd.md)
#### [$ smoothie](https://github.com/SayadPervez/AMD-SEPERATE-DOCUMENTATION/blob/master/DataScience/smoothie.md)
#### [$ visualizeSmoothie](https://github.com/SayadPervez/AMD-SEPERATE-DOCUMENTATION/blob/master/DataScience/visualizeSmoothie.md)
___
### [ >> Data storage and extraction functions for AMD known as AMD CDB which stands for 'AMD Custom DataBase': ](https://github.com/SayadPervez/AMD-SEPERATE-DOCUMENTATION/blob/master/AMD%20CDB.md)
#### [Intro to AMD CDB](https://github.com/SayadPervez/AMD-SEPERATE-DOCUMENTATION/blob/master/DataBase/AMD%20Custom%20DataBase%20Methods.md)
#### [save](https://github.com/SayadPervez/AMD-SEPERATE-DOCUMENTATION/blob/master/DataBase/save.md)
#### [appendSave](https://github.com/SayadPervez/AMD-SEPERATE-DOCUMENTATION/blob/master/DataBase/appendSave.md)
#### [rewriteSave](https://github.com/SayadPervez/AMD-SEPERATE-DOCUMENTATION/blob/master/DataBase/rewriteSave.md)
#### [extract](https://github.com/SayadPervez/AMD-SEPERATE-DOCUMENTATION/blob/master/DataBase/extract.md)
#### [extractX](https://github.com/SayadPervez/AMD-SEPERATE-DOCUMENTATION/blob/master/DataBase/extractX.md)
#### [extractY](https://github.com/SayadPervez/AMD-SEPERATE-DOCUMENTATION/blob/master/DataBase/extractY.md)
___
___
### [Some projects that can be done with this module !!](https://github.com/SayadPervez/AMD-SEPERATE-DOCUMENTATION/blob/master/Examples.md)
___
___
![Mr_Handsome](https://github.com/SayadPervez/AMD-SEPERATE-DOCUMENTATION/blob/master/IMG_20190225_150001_460.jpg?raw=true)
### Sayad Pervez - the solo developer of AMD Module !
### E-Mail : [pervez2504@gmail.com](pervez2504@gmail.com)
___
___
