# About the dataset

We compile a total of 3807 transient objects (AGN,BZ,CV,SN and OTHER) and 12500 non-transient objects (NON, located [here](https://github.com/MachineLearningUniandes/TAO_non-transients)).

| Class | Total Objects |
|:-----:|:-------------:|
|  AGN  |      606      |
|   BZ  |      239      |
|   CV  |      772      |
|   SN  |      1372     |
| OTHER |      818      |
|  NON  |     12500     |


## Transients Objects

For the Transients objects, you can find in the fits images' headers the next information: 

| Header Dict | Description                                  | Type |
|-------------|----------------------------------------------|------|
| CRTS_ID     | Catalina Real-time Transient Survey  ID.     | str  |
| RA_(J2000)  | Right Ascension (degrees).                   | float  |
| Dec_(J2000) | Declination (degrees).                       | float  |
| N_Images    | Total number of images for this CRTS ID.     | int  |
| UT_Date     | Discovery Date.                              | float  |
| Mag         | Unfiltered CSS magnitude.                    | float  |
| CSS_Images  | Pre and post-discovery images.               | int  |
| SDSS        | Covered by SDSS DR-12 (yes/no).              | str  |
| Others      | Images from SDSS, Palomar-Quest, DSS, 2MASS. | int  |
| Followed    | P60 follow up.                               | str  |
| Last        | Last data update.                            | str  |
| LC          | Curren CSS lightcurve.                       | int  |
| FC          | Finding chart (yes/no).                      | str  |
| Class       | Transient classification.                    | str  |


In hdu 1, you can find a table that contains information to identify the images by sequence, date, MJD, Field ID, observation number in the sequence, or cutout.

| Table of Content HDU:1 (Table) | Description                                                                | Type |
|-------------------------|-----------------------------------------------------------------------------------|------|
| HDU_Ext                 | Extension number of the image in the fits file.                                   | int  |
| Set_Number              | Stands for the sequence (or set number).                                          | str  |
| Date                    | Date of observation in YYMMMDD format.                                            | str  |
| MJD                     | Modified Julian Date.                                                             | float  |
| Field_ID                | Field identifier.                                                                 | str  |
| Obs_In_Seq              | Refers to the observation’s number in the sequence.                               | str  |
| Cutout                  | The cutout matrix location. Each cutout covers an area of ABOUT 5 x 5 arcminutes. | str  |


# How to read the dataset?

An example of how to read the data set is [here](../master/data/Read_dataset.ipynb).
