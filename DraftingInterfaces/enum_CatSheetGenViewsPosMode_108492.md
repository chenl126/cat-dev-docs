# CatSheetGenViewsPosMode (Enumeration)

**_Positioning mode values for generative views inside the sheet._**
The positioning mode for a given sheet determines the generative views position behavior when an update is requested. Notice: the position of generative views is usually the position of the image of the center of gravity of the 3D data.

`catFixedCG`      the position of the image of the center of gravity of the 3D data remains the same after an update.  `catFixedAxis`      the position of the image of the center of gravity is modified so that existing geometries don't move after an update.