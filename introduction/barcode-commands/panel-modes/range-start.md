# RANGE START of serial numbers (from ... to)


## About the mode
 
This mode is introduced in Version 2019.1. It is used for **entering a starting serial number** when creating a range of serial numbers starting from a particular serial number and ending to a particular serial number. 

After the selection of the starting number, the system automatically switches to **[RANGE END of serial numbers (from ... to)](range-end.md)** mode in which we should enter the ending serial number for the range we would like to create.

#### Example: We want to create a range of serial numbers starting from serial number ‘XB0008’ and ending to a serial number ‘XB0012’. 

In this case, we could:

> [!NOTE] 
> 
> The product has already been selected manually or through the [Main mode](main-mode.md).

1. Select the **RANGE START** and enter the starting number ’XB0008’.
2. The system automatically switches to **[RANGE END](range-end.md)** mode - enter ’XB0012’

=> the system will create 5 serial numbers - XB0008, XB0009, XB0010, XB0011 and XB0012.

Alternatively, we could skip these steps and use only the **[RANGE END](range-end.md)** to complete the task. In this case, we should enter the string ‘XB0008 ... XB0012’ which will be recognized the same way.
 
## Mode selection
 
The **RANGE START of Serial numbers (from ... to)** mode can be selected:

- **manually** from the dropdown list in the Barcode panel.  
- **manually** by entering the **fast command #RNGSTART#** in the main field when panel is operating in one of the serial number modes.
- **automatically** after the selection of the product through the **[Main mode](main-mode.md)** - 

as long as the _Use serial numbers_ option from the Barcode settings is activated **AND** the product ‘_Is serialized_’ **AND** the form type is ‘Receive’ (for more information, see ‘Form types and Mode selection’ in @barcode-commands ) 

**AND:**

-it is the first use of the panel after opening the form **AND** the current mode is selected in the field _Default mode for serial numbers input_ from the Barcode panel settings 
 
**OR**

-it is **NOT** the first use of the panel after opening the form **AND** the current mode is the last used mode for serial numbers input.
 
## Mode operation
 
If **’RANGE START** mode is selected, when scanning/adding a serial number in the main field, the following actions are completed by the system:

**(1)** If the form type is different from ‘Receive’ - throw **Message1** and return to the previous mode.  Else => **(2)**

**(2)** Add the scanned/added record in the field _Serial Numbers_ followed by ellipsis (three dots ‘...’).

> [!NOTE] 
>
> If the field _Serial numbers_ already has a value, the value is cleared.

**(3)** Proceed to mode **[RANGE END](range-end.md)**.
 
**Message1:**<br>
The ‘{0}’ mode is available only when all lines in the form are with movement type ‘Receipt’.<br>
{0} - ModeName

