# LIST of serial numbers (Finally - scan # ADD #)

## About the mode
 
The LIST of serial numbers (Finally - scan # ADD #) Mode is used for entering a list  of serial numbers. If we are receiving goods, this mode can be used for creating new serial numbers automatically. 
 
## Mode selection
 
The ‘LIST’ of Serial numbers (Finally - scan # ADD #)" mode can be selected:
- **manually** from the drop down list in the Barcode panel.  
- **manually** by entering the **fast command #LIST#** in the main field when the panel is operating in one of the serial number modes.
- **automatically** after the selection of the product through the **Main (barcode/command/came) mode** - 

if the ‘Use serial numbers option in the Barcode settings is activated **AND** the products ‘Is serialized’ **AND**:
- it is the first use of the panel after opening the form **AND** the current mode is selected in the field ‘Default mode for serial numbers input’ in the Barcode panel settings 

**OR**

-  it is **NOT** the first use of the panel after opening the form **AND** the current mode is the last used mode for serial numbers input.
 
 
## Mode operation
 
 If the List mode is set, when scanning/adding a serial number in the main field the following actions are completed:
**(0)** scan # ADD # => **(9)**

**Note:** This command means that we want to stop listing serial numbers and to add new product lines. Here, this command is included only for clarity. This is a global command and it will be executed regardless of the mode.

**(1)** Check the form type. If the form type = ‘Receive’ (for more information see ‘Form types and Mode selection’ section in topic **Barcode commands**), then =>** (7)**

**(2)** Look for the serial numbers related to the product set in the field Product. If the serial number exists for the selected product =>** (5)**

**(3)** The serial number does not exist. Clear the code. Wait for another serial number.

**(4)** STOP

**(5)** Add the serial number (separated with comma) to the list of serial numbers in the field ‘Serial numbers’.

**(6)** STOP

**(7)** Create a new serial number. Then =>**(5)**

**(8)** STOP

**(9)** Add multiple product lines - one for each serial number listed in the filed ‘Serial numbers’.


