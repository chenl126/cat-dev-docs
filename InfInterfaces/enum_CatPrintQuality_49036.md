# CatPrintQuality (Enumeration)

**_Print quality._**
It is used by the [PageSetup](../InfInterfaces/interface_PageSetup_17718.md) object for document printing. The print quality ranges from `catPrintQualityDraft` to `catPrintQualityHigh` and applies to shaded images. `catPrintQualityDraft` is the lowest quality and creates images with the screen resolution (It is for example the Quality 0 for HP-GL/2.) `catPrintQualityHigh` prints images at the maximum printer resolution. The other print qualities are somewhere in between.

**Values:**

` catPrintQualityDraft`      The print quality is acceptable for drafts
` catPrintQualityLow`      The print quality is low
` catPrintQualityMedium`      The print quality is medium
` catPrintQualityHigh`      The print quality is high
` catPrintQualityCustom`      The print quality is custom