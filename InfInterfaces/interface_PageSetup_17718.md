# PageSetup (Object)

**_Represents the page setup._**
The page setup is the object that stores data which defines how your documents and images are actually printed on paper. This data includes namely the paper size, the orientation, the bottom, top, right, and left margins, the zoom factor, the banner, and the printing quality.

## Properties

### Property **Banner**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns or sets the banner text. The banner text is added to the print and can include variables, such as the user who prints, the date and time of printing. Available variables are:

$USER     The user name $HOST     The workstation name $SCALE     The print scale $TIME     The print time $DATE     The print date $DAY     The print day $MONTH     The print month $YEAR     The print year  The default banner is:

```VBScript
Printed by $USER on $DATE $TIME

```

**Example:**      This example sets the banner text to the following:
Printed by $USER at scale $SCALE on $MONTH/$DAY/$YEAR
for the `SetupForMyPrint` page setup.

```VBScript
SetupForMyPrint.Banner = "Printed by $USER at scale $SCALE on $MONTH/$DAY/$YEAR"

```

### Property **BannerPosition**( ) As [CatBannerPosition](../InfInterfaces/enum_CatBannerPosition_61893.md)

Returns or sets the banner position. The banner can be located on the top, bottom, left, or right side of the page. `catBannerPositionNone` removes the banner.

**Example:**      This example sets the banner on the top side of the page for the `SetupForMyPrint` page setup.

```VBScript
SetupForMyPrint.BannerPosition = CatBannerPositionTop

```

### Property **BannerSize**( ) As float

Returns or sets Banner Size. Banner size could range from 0.1 mm to 10.0 mm Default value is 2.4 mm

**Example:**      This example sets banner size for the `SetupForMyPrint` page setup.

```VBScript
SetupForMyPrint.BannerSize = 1.1

```

### Property **Bottom**( ) As float

Returns or sets the lower left corner location with respect to the bottom of the sheet of paper. This is the distance of the document or the image to print lower left corner to the paper lower left corner.

**Example:**      This example sets the location of the lower left corner of the document or the image to print at 40 mm from the paper lower left corner for the `SetupForMyPrint` page setup.

```VBScript
SetupForMyPrint.Bottom = 40

```

### Property **BottomMargin**( ) As float

Returns or sets the bottom margin. The bottom margin is a strip in which nothing is printed, located at the bottom of the page, which height is expressed in mm.

**Example:**      This example sets the bottom margin for the `SetupForMyPrint` page setup to 10 mm.

```VBScript
SetupForMyPrint.BottomMargin = 10

```

### Property **Color**( ) As [CatPrintColor](../InfInterfaces/enum_CatPrintColor_36192.md)

Returns or sets the color mode to use when printing.

**Example:**      This example sets the color mode to GreyScale for the `SetupForMyPrint` page setup.

```VBScript
SetupForMyPrint.Color = catColorGreyScale

```

### Property **Dpi**( ) As float

Returns or sets the printing dpi.

**Example:**      This example sets the printing dpi for the `SetupForMyPrint` page setup.

```VBScript
SetupForMyPrint.Dpi = 150.

```

### Property **Gamma**( ) As float

Returns or sets Gamma factor for print. Gamma value could range from 0.1 to 5.0 Default value is 1.0

**Example:**      This example sets Gamma factor for the `SetupForMyPrint` page setup.

```VBScript
SetupForMyPrint.Gamma = 1.2

```

### Property **Left**( ) As float

Returns or sets the lower left corner location with respect to the left of the sheet of paper. This is the distance of the document or the image to print lower left corner to the paper lower left corner.

**Example:**      This example sets the location of the lower left corner of the document or the image to print at 25 mm from the paper lower left corner for the `SetupForMyPrint` page setup.

```VBScript
SetupForMyPrint.Left = 25

```

### Property **LeftMargin**( ) As float

Returns or sets the left margin. The left margin is a strip in which nothing is printed, located at the left of the page, which width is expressed in mm.

**Example:**      This example sets the left margin for the `SetupForMyPrint` page setup to 10 mm.

```VBScript
SetupForMyPrint.LeftMargin = 10

```

### Property **LineCap**( ) As [CatPrintLineCap](../InfInterfaces/enum_CatPrintLineCap_45879.md)

Returns or sets Line cap for print. Refer to [CatPrintLineCap](../InfInterfaces/enum_CatPrintLineCap_45879.md) Default value is catPrintFlat

**Example:**      This example sets Line cap for the `SetupForMyPrint` page setup.

```VBScript
SetupForMyPrint.LineCap = catPrintFlat

```

### Property **LineTypeOverlappingCheck**( ) As boolean

Returns or sets text Line type overlap check option for print. Default value is FALSE

**Example:**      This example sets Line type overlapping check option for the `SetupForMyPrint` page setup.

```VBScript
SetupForMyPrint.LineTypeOverlappingCheck = True

```

### Property **LineTypeSpecification**( ) As [CatPrintLineSpecification](../InfInterfaces/enum_CatPrintLineSpecification_131036.md)

Returns or sets Line type specification for print. Refer to [CatPrintLineSpecification](../InfInterfaces/enum_CatPrintLineSpecification_131036.md) Default value is catPrintAbsolute

**Example:**      This example sets Line type specification for the `SetupForMyPrint` page setup.

```VBScript
SetupForMyPrint.LineTypeSpecification = catPrintAbsolute

```

### Property **LineWidthSpecification**( ) As [CatPrintLineSpecification](../InfInterfaces/enum_CatPrintLineSpecification_131036.md)

Returns or sets Line width specification for print. Refer to [CatPrintLineSpecification](../InfInterfaces/enum_CatPrintLineSpecification_131036.md) Default value is catPrintAbsolute

**Example:**      This example sets Line width specification for the `SetupForMyPrint` page setup.

```VBScript
SetupForMyPrint.LineWidthSpecification = catPrintAbsolute

```

### Property **Logo**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns or sets the file containing the logo image. The logo is printed with the banner.

**Example:**      This example sets the logo file to the following file: `e:\users\psr\Images\Logo.tif` for the `SetupForMyPrint` page setup.

```VBScript
SetupForMyPrint.Logo = "e:\users\psr\Images\Logo.tif"

```

### Property **LogoVisibility**( ) As boolean

Returns or sets LogoVisibility option for print. Default value is FALSE

**Example:**      This example sets LogoVisibility option for the `SetupForMyPrint` page setup.

```VBScript
SetupForMyPrint.LogoVisibility = True

```

### Property **MaximumSize**( ) As boolean

Returns or sets whether the document or the image should be printed at the maximum size with respect to the page size and margins.
**True** if the document or the image is printed with the maximum size. This overrides the location properties, that is Left and Bottom, and the Zoom property values.

**Example:**      This example requests to print the document or the image with the `SetupForMyPrint` page setup at maximum size.

```VBScript
SetupForMyPrint.MaximumSize = True

```

### Property **Orientation**( ) As [CatPaperOrientation](../InfInterfaces/enum_CatPaperOrientation_77334.md)

Returns or sets the paper orientation.

**Example:**      This example sets the paper orientation for the `SetupForMyPrint` page setup to `catPaperLandscape`.

```VBScript
SetupForMyPrint.Orientation = catPaperLandscape

```

### Property **PaperHeight**( ) As float

Returns or sets the paper height.

**Example:**      This example sets the page height for the `SetupForMyPrint` page setup to 297 mm..

```VBScript
SetupForMyPrint.PaperHeight = 297

```

### Property **PaperSize**( ) As [CatPaperSize](../InfInterfaces/enum_CatPaperSize_30452.md)

Returns or sets the paper size.

**Example:**      This example sets the page size for the `SetupForMyPrint` page setup to `catPaperA4`.

```VBScript
SetupForMyPrint.PaperSize = catPaperA4

```

### Property **PaperWidth**( ) As float

Returns or sets the paper width.

**Example:**      This example sets the page width for the `SetupForMyPrint` page setup to 210 mm..

```VBScript
SetupForMyPrint.PaperWidth = 210

```

### Property **PrintRenderingMode**( ) As [CatPrintRenderingMode](../InfInterfaces/enum_CatPrintRenderingMode_91712.md)

Returns or sets the printing rendering mode.

**Example:**      This example sets the printing rendering mode for the `SetupForMyPrint` page setup.

```VBScript
SetupForMyPrint.PrintRenderingMode = CatPrintRenderingModeDefault

```

### Property **Quality**( ) As [CatPrintQuality](../InfInterfaces/enum_CatPrintQuality_49036.md)

Returns or sets the printing quality. Refer to [CatPrintQuality](../InfInterfaces/enum_CatPrintQuality_49036.md)

**Example:**      This example sets the printing quality to draft for the `SetupForMyPrint` page setup.

```VBScript
SetupForMyPrint.Quality = catPrintQualityDraft

```

### Property **RightMargin**( ) As float

Returns or sets the right margin. The right margin is a strip in which nothing is printed, located at the right of the page, which width is expressed in mm.

**Example:**      This example sets the right margin for the `SetupForMyPrint` page setup to 12 mm.

```VBScript
SetupForMyPrint.RightMargin = 12

```

### Property **Rotation**( ) As [CatImageRotation](../InfInterfaces/enum_CatImageRotation_54272.md)

Returns or sets the rotation of the document or the image to print. Rotations angles can be 0, 90, 180, and 270 degrees counted clockwise.

**Example:**      This example sets the rotation to 90 degrees clockwise for the `SetupForMyPrint` page setup.

```VBScript
SetupForMyPrint.Rotation = catImageRotation90

```

### Property **Scaling1To1**( ) As boolean

Returns or sets whether the document or the image should be printed with a zoom factor equals to 1 and the image to print lower left corner on the paper lower corner.
**True** if the document or the image is printed with the zoom factor equals to 1 and the image to print lower left corner on the paper lower corner. This overrides the location properties, that is Left and Bottom, and the Zoom property values.

**Example:**      This example requests to print the document or the image with the `SetupForMyPrint` page setup.

```VBScript
SetupForMyPrint.Scaling1To1 = True

```

### Property **TextBlanking**( ) As boolean

Returns or sets the text blanking option in print Text will be printed in blanking rectangle Default value is FALSE

**Example:**      This example sets the text blanking option for the `SetupForMyPrint` page setup.

```VBScript
SetupForMyPrint.TextBlanking = True

```

### Property **TextScaling**( ) As boolean

Returns or sets text scaling option for print. Default value is TRUE

**Example:**      This example sets text scaling option for the `SetupForMyPrint` page setup.

```VBScript
SetupForMyPrint.TextScaling = True

```

### Property **TopMargin**( ) As float

Returns or sets the top margin. The top margin is a strip in which nothing is printed, located at the top of the page, which height is expressed in mm.

**Example:**      This example sets the top margin for the `SetupForMyPrint` page setup to 15 mm.

```VBScript
SetupForMyPrint.TopMargin = 15

```

### Property **Use3DAccuracy**( ) As boolean

Returns or sets Use3DAccuracy option for print. Default value is FALSE

**Example:**      This example sets Use3DAccuracy option for the `SetupForMyPrint` page setup.

```VBScript
SetupForMyPrint.Use3DAccuracy = True

```

### Property **UseImageSize**( ) As boolean

Returns or sets the paper size to the image size.

**Example:**      This example sets the paper size to image size for the `SetupForMyPrint` page setup.

```VBScript
SetupForMyPrint.UseImageSize = True

```

### Property **WhiteVectorsInBlack**( ) As boolean

Returns or sets the white vectors in black option. white vectors will be printed in black if set to True Default value is TRUE

**Example:**      This example sets the Print White Vectors In Black option for the `SetupForMyPrint` page setup.

```VBScript
SetupForMyPrint.WhiteVectorsInBlack = True

```

### Property **Zoom**( ) As float

Returns or sets the zoom factor to use when printing.

**Example:**      This example sets the zoom factor to 1.5 for the `SetupForMyPrint` page setup.

```VBScript
SetupForMyPrint.Zoom = 1.5

```