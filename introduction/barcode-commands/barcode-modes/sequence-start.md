# SEQUENCE START of Serial numbers (from ... count)


 ## About the mode
 
 
This mode is introduced in Version 2019.1. It is used for **entering a starting serial number** when creating a sequence of an exact count of serial numbers starting from a particular serial number. After the selection of the starting number the system automatically switches to ‘SEQUENCE END of Serial numbers (from ... count)’ mode in which we should enter the count of numbers that we would like to create.

***Example:*** We want to create 5 serial numbers starting from serial number ‘XB0008’. In this case we could:

***Note:*** The product has already been selected manually or through the **Main (barcode/command/name) mode**.
1. Select the ‘SEQUENCE START of Serial numbers (from ... count)’ and enter the starting number ’XB0008’.
2. The system automatically switches to **‘SEQUENCE END of Serial numbers (from ... count)‘** - enter ‘5’
=> the system will create 5 serial numbers - XB0008, XB0009, XB0010, XB0011 and XB0012.

Alternatively, we could skip these steps and use only the ‘SEQUENCE END of Serial numbers (from ... count)’ mode to complete the task. In this case we should enter the string ‘XB0008 ... 5’ which will be recognized in the same way (for more information see **SEQUENCE END of Serial numbers (from ... count)**).
 
## Mode selection
 
The ‘SEQUENCE START of Serial numbers (from ... count)’ mode can be selected:
- **manually** from the drop down list in the Barcode panel.  
- **manually** by entering the **fast command #SEQSTART#**  in the main field when the panel is operating in one one of the serial number modes.
- **automatically** after the selection of the product through the **Main (Barcode/Command/Name) mode** - 

if the ‘Use serial numbers’ option in the Barcode settings is activated **AND** the product ‘Is serialized’ **AND** the form type is ‘Receive’ (for more information see ‘Form types and Mode selection’ section in topic **Barcode commands**) **AND:**
- * it is the first use of the panel after opening the form **AND** the current mode is selected in the field ‘Default mode for serial numbers input’ in the Barcode panel settings 

**OR**

- *  it is **NOT** the first use of the panel after opening the form **AND** the current mode is the last used mode for serial numbers input.
 
## Mode operation
 
If **’SEQUENCE START of Serial numbers (from ... count)’** mode is selected, **when scanning/adding** a serial number in the main field the following actions **are completed by the system**:

**(1)** If the form type is different from ‘Receive’ - throw **Message1** and return to the previous mode.  Else =>**(2)**</br>

**(2)** Add the scanned/added record in the field ‘Serial numbers’ followed by ellipsis (three dots ‘...’).</br>

**Note:** If the field ‘Serial numbers’ already has a value, the value is cleared.</br>

**(3)** Proceed in  **‘SEQUENCE END of Serial numbers (from ... count)‘** mode.</br>
 
**Message1:**

The ‘{0}’ mode is available only when all lines in the form are with movement type ‘Receipt’.</br>
, {0} - ModeName

