# CatPrinterDirState (Enumeration)

**_Printer directory state._**
It is used by the [PrintersSettingAtt](../InfInterfaces/interface_PrintersSettingAtt_69832.md) object for modify the printers setting. Each directory can be protected to prevent user access to the printers it contains. The state could be "CATPrinterDirFree" or "CATPrinterDirProtect"

**Values:**

` CATPrinterDirFree`      The parameters of each printer included in the directory can be changed, and the printers can be removed.
` CATPrinterDirProtect`      The parameters of each printer included in the directory cannot be changed.