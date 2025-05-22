# Printer (Object)

**_Represents a printer handled by the printing subsystem._**
This object is read only and gives access to some properties of the printer.

## Properties

### Property **DeviceName**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

Returns the printer device name.

**Example:**      This example displays the device name of the `myPrinter` printer.

```VBScript
MsgBox myPrinter.DeviceName

```

### Property **Orientation**( ) As [CatPaperOrientation](../InfInterfaces/enum_CatPaperOrientation_77334.md) (Read Only)

Returns or sets the default paper orientation.

**Example:**      This example retrieves in `DefaultPaperOrientation` the default paper orientation of the `myPrinter` printer.

```VBScript
Dim DefaultPaperOrientation As CatPaperOrientation
DefaultPaperOrientation = myPrinter.Orientation

```

### Property **PaperHeight**( ) As float (Read Only)

Returns the default paper height.

**Example:**      This example retrieves in `Height` the default paper height of the `myPrinter` printer.

```VBScript
Dim Height
Height = myPrinter.PaperHeight

```

### Property **PaperSize**( ) As [CatPaperSize](../InfInterfaces/enum_CatPaperSize_30452.md) (Read Only)

Returns the default paper size.

**Example:**      This example retrieves in `DefaultPaperSize` the default paper size of the `myPrinter` printer.

```VBScript
Dim DefaultPaperSize As CatPaperSize
DefaultPaperSize = myPrinter.PaperSize

```

### Property **PaperWidth**( ) As float (Read Only)

Returns the default paper width.

**Example:**      This example retrieves in `Witdh` the default paper width of the `myPrinter` printer.

```VBScript
Dim Width As float
Width = myPrinter.PaperWidth

```