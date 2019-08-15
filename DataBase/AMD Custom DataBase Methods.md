# AMD - Arduino Matplotlib DataScience
## AMD Custom DataBase(AMD CDB) Methods:

### All functions of the DataBase part take in hybrids. As already discussed, hybrids contain X and Y values. They way they are saved in this module is a bit unique. A text File is used to save AMD CDB. In an AMD CDB file, each line represents a set of X and Y values. X values are enclosed within '>>' and '<<' symbols. Y values are enclosed within '))' and '((' symbols. These are known as capsules. At the end of each set of save, an underscore is added. Fortunately anything outside these capsules won't matter.

### One such file is described below:
![AMD CDB](https://github.com/SayadPervez/Arduino_Master_Delta/blob/master/AMD%20CDB.JPG?raw=true)
