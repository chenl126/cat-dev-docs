# DraftingPageSetup (Object)

**_Represents the page setup for the drawing documents._**
The page setup is the object that stores data which defines how your documents and images are actually printed on paper. This data includes namely the paper size, the orientation, the bottom, top, right, and left margins, the zoom factor, the banner, the printing quality, the choice of the best orientation, and the choice to fit either the drawing sheet format or the printer format.

## Properties

### Property **ChooseBestOrientation**(| ) As boolean

   Activates or deactivates the choice of the best orientation.

**Example:**      This example requests the best orientation to be chosen for `MySheet`.

```VBScript
     MySheet.DrawingPageSetUp.ChooseBestOrientation = TRUE

```

### Property **FitToPrinterFormat**( ) As boolean

   Fits the format of the print to the printer format.

**Example:**      This example turns this calculation on.

```VBScript
     MySheet.DrawingPageSetUp.FitToPrinterFormat = TRUE

```

### Property **FitToSheetFormat**( ) As boolean

   Fits the format of the print to the sheet format.

**Example:**      This example turns this calculation on.

```VBScript
     MySheet.DrawingPageSetUp.FitToSheetFormat = TRUE

```