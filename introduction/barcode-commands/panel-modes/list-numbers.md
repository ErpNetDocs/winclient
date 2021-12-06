# LIST of serial numbers (Finally - scan # ADD #)

## About the mode
 
Used for entering a list of serial numbers. If we are receiving goods, it can be used for creating new serial numbers automatically. 
 
## Mode selection
 
The mode can be selected:

- **manually** - from the dropdown list in the Barcode panel.  
- **manually** - by entering the **fast command #LIST#** in the main field when the panel is operating in one of the serial number modes.
- **automatically** - after the selection of the product through the **[Main mode](main-mode.md)** -
as long as the _Use serial numbers_ option from the barcode settings is activated **AND** the product ‘_Is serialized_’ **AND**: 
<br/>\- it is the first use of the panel after opening the form **AND** the current mode is selected in the field *Default mode for serial numbers input* in the **Barcode** panel settings 
<br/>**OR**
<br/>\-  it is **NOT** the first use of the panel after opening the form **AND** the current mode is the last used mode for serial numbers input.
 
 
## Mode operation
 
 If **List** mode is set, when scanning/adding a serial number in the main field, the following actions are completed:
 
**(0)** scan # ADD # => **(9)**

> [!NOTE]
> 
> This command means that we want to stop listing serial numbers and add new product lines. Here, the command is included only for clarity. This is a global command and it will be executed regardless of the mode.

**(1)** Check the form type. If the form type = ‘Receive’, then =>** (7)** 

For more information see ‘Form types and mode selection’ in @barcode-commands.

**(2)** Look for the serial numbers related to the product set in the field _Product_. If the serial number exists for the selected product =>** (5)**

**(3)** The serial number does not exist. Clear the code. Wait for another serial number.

**(4)** STOP

**(5)** Add the serial number (separated with comma) to the list of serial numbers in the field _Serial Numbers_.

**(6)** STOP

**(7)** Create a new serial number. Then =>**(5)**

**(8)** STOP

**(9)** Add multiple product lines - one for each serial number listed in the field _Serial Numbers_.


