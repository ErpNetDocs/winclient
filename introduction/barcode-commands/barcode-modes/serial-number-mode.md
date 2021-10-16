# Serial number mode

## About the mode
The Serial number mode is used for entering a single serial number. If we are receiving goods this mode can be used for creating new serial numbers automatically. 
 
## Mode selection
 
The ‘Serial number mode’ mode can be selected:
- **manually** from the drop down list in the Barcode panel.  
- **manually** by entering the **fast command #SERIAL#** in the main field when panel is operating in one one of the serial number modes.
- **automatically** after the selection of the product through the **‘Main (barcode/command/name) mode** - 

if the ‘Use serial numbers’ option in the Barcode settings is activated **AND** the products ‘Is serialized’ **AND:**
 
 -it is the first use of the panel after opening the form **AND** the current mode is selected in the field ‘Default mode for serial numbers input’ in the Barcode panel settings 

**OR**

-it is **NOT** the first use of the panel after opening the form **AND** the current mode is the last used for serial numbers input.
 
## Mode operation
 
 If this mode is set, **when scanning/adding** a serial number in the main field, the following actions are **completed by the system**:

**(1)** Look through the serial numbers related to the product set in the field Product. If the serial number exists for the selected product => **(5)**

**(2)** The serial number does not exist. If the form type = ‘Receive’ (for more information see ‘Form types and Mode selection’ section in topic **Barcode commands**), a new serial number can be  created. Then => **(5)**

**(3)** If the form type = ‘Issue’ or ‘Indefinite’ (for more information see ‘Form types and Mode selection’ section in topic **Barcode commands**). Clear the code. Wait for another serial number.

**(4)** STOP

**(5)** Create a new line using current values of the fields in the panel.

