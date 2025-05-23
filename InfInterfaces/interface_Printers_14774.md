# Printers (Collection)

**_A collection of all the Printer objects managed by the application._**

## Methods

### Func **Item**(| [CATVariant](../System/typedef_CATVariant_20656.md) | `iIndex`) As [CATIAPrinter](../InfInterfaces/interface_Printer_11274.md)

   Returns a printer using its index or its device name from the Printers collection.

**Parameters:**

` iIndex`      The index or the name of the printer to retrieve from the collection of printers. As a numerics, this index is the rank of the printer in the collection. The index of the first printer in the collection is 1, and the index of the last printer is Count. As a string, it is the DeviceName of the printer.

**Returns:**      The retrieved printer  **Example:**      This example returns in `ThisPrinter` the third printer in the collection, and in `ThatPrinter` the printer named `LaserPrinter`.

```VBScript
     Dim ThisPrinter As Printer
     Set ThisPrinter = CATIA.Printers.Item(3)
     Dim ThatPrinter As Printer
     Set ThatPrinter = CATIA.Printers.Item("LaserPrinter")

```