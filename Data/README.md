# About the Datasets Used

## Hawks 

This data contains 908 observations for 3 species of hawks (which will formulate the classes) and 19 features including age, sex, wing length, body weight, tail length, etc. As a result, this dataset is suited for the classification tasks of supervised learning. It can even be used for regression.

More details about this dataset and visualizations of the relevant features for the machine learning algorithms can be found in the `hawks_analysis.ipynb` [notebook in this directory](https://github.com/kary5678/INDE-577/blob/main/Data/hawks_analysis.ipynb). Here is a list of all the features in the original dataset; note that not all will be used, the reasoning is discussed in the aforementioned data exploration notebook.

1. `Month` - an integer representing a month (March is denoted by 3)
2. `Day` - an integer representing the date in the month
3. `Year` - an integer representing the year, ranging from 1992 to 2003
4. `CaptureTime` - time of capture, denoted by HH:MM format
5. `ReleaseTime` - time of release, denoted by HH:MM format
6. `BandNumber` - a string of the code for the hawk's ID band 
7. `Species` - a string denoting the species of the hawk, as follows:
   * `RT`: Red-tailed
   * `CH`: Cooper's
   * `SS`: Sharp-Shinned
8. `Age` - a string categorizing the age of the hawk, as follows:
   * `A`: Adult
   * `I`: Immature
9. `Sex` - a string categorizing the sex of the hawk, as follows:
   * `F`: Female
   * `M`: Male
10. `Wing`: numeric, length (in mm) of the primary wing
11. `Weight`: numeric, body weight (in gm)
12. `Culmen`: numeric, length (in mm) of the upper bill from the tip to where it bumps into the fleshy part of the bird
13. `Hallux`: numeric, length (in mm) of the killing talon
14. `Tail`: numeric, tail length (in mm)
15. `StandardTail`: numeric, standard measurement of tail length (in mm)
16. `Tarsus`: numeric, length of the basic foot bone (in mm)
17. `WingPitFat`: numeric, amount of fat in the wing pit
18. `KeelFat`: numeric, amount of fat on the breastbone
19. `Crop`: numeric, amount of material in the crop from 0=empty to 1=full

You can find this dataset from the original source [here.](https://r-data.pmagunia.com/dataset/r-dataset-package-stat2data-hawks)
