# Serial number mode

## About the mode

This mode is used for entering a single serial number. If we are receiving goods, this mode can be used for creating new serial numbers automatically. 
 
## Mode selection
 
The **Serial number mode** mode can be selected:

- **manually** from the dropdown list in the Barcode panel.  
- **manually** by entering the **fast command #SERIAL#** in the main field when the panel is operating in one one of the serial number modes.
- **automatically** after the selection of the product through the [Main mode](https://docs.erp.net/winclient/introduction/barcode-commands/barcode-modes/main-mode.html) 

as long as the _Use serial numbers_ option from the Barcode settings is activated **AND** the product ‘_Is serialized_’ 

**AND:**
 
-it is the first use of the panel after opening the form **AND** the current mode is selected in the field _Default mode for serial numbers input_ from the Barcode panel settings 

**OR**

-it is **NOT** the first use of the panel after opening the form **AND** the current mode is the last used for serial numbers input.
 
## Mode operation
 
 If this mode is set, when scanning/adding a serial number in the main field, the following actions are completed by the system:

**(1)** Look through the serial numbers related to the product set in the field _Product_. If the serial number exists for the selected product => **(5)**

**(2)** The serial number does not exist. If the form type = ‘Receive’, a new serial number can be created. Then => **(5)**.

**(3)** If the form type = ‘Issue’ or ‘Indefinite’. Clear the code. Wait for another serial number.

For more information, see ‘Form types and Mode selection’ in **[Barcode commands](https://docs.erp.net/winclient/introduction/barcode-commands/index.html)**

**(4)** STOP

**(5)** Create a new line using current values of the fields in the panel.

