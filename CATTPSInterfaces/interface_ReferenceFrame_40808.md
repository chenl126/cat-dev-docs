# ReferenceFrame (Object)

**_Interface designed to manage reference frame associated to a TPS._**
Reference frame is composed of three boxes.

```VBScript
                             Reference Frame
                            /
                      _____|_____
                     /           \
             ---------------------
             |   |   |Box|Box|Box|
             |   |   | 1 | 2 | 3 |
             ---------------------

```VBScript

        **AllDatumsSimple**
          Retrieves all datums simple used in Reference Frame.

        **Frame**
          Retrieves Frame of the TPS.

        **SetFrame**
          Set Frame of the TPS.

    ## Properties

    ### Property **AllDatumsSimple**(| ) As [CATIAAnnotations](../CATTPSInterfaces/interface_Annotations_27300.md)  (Read Only)

     Retrieves all datums simple used in Reference Frame.

       **Parameters:**

         opiListDatumsSimple
                All objects of the collection

     Methods

### Sub **Frame**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  oFirstBox,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  oSecondBox,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  oThirdBox)

     Retrieves Frame of the TPS.

       **Parameters:**

         oFirstBox

         oSecondBox

         oThirdBox
                Texts in first, second and third boxes.

### Sub **SetFrame**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  iFirstBox,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  iSecondBox,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  iThirdBox)

     Set Frame of the TPS.

       **Parameters:**

         oFirstBox

         oSecondBox

         oThirdBox
                Texts in first, second and third boxes.