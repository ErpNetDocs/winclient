# RANGE END of serial numbers (from ... to)


## About the mode
 
 
This mode is introduced in Version 2019.1. It is used for **entering an ending serial number** when creating a range of serial numbers starting from a particular serial number and ending to a particular serial number.

For entering a start number, use **[RANGE START of serial numbers (from ... to)](https://docs.erp.net/winclient/introduction/barcode-commands/barcode-modes/range-start.html)**. 

***Example:*** We want to create a range of serial numbers starting from serial number ‘XB0008’ and ending to‘XB0012’. 

In this case, we can:

> [!NOTE]
> 
> The product has already been selected manually or through the [Main mode](https://docs.erp.net/winclient/introduction/barcode-commands/barcode-modes/main-mode.html).

**Method 1:**

1. Select the **[RANGE START](https://docs.erp.net/winclient/introduction/barcode-commands/barcode-modes/range-start.html)** mode and enter the starting number ’XB0008’.

2. The system automatically switches to **RANGE END** mode - enter ’XB0012’

=> it will create 5 serial numbers - XB0008, XB0009, XB0010, XB0011 and XB0012.

**Method 2:** 

Alternatively, we could use only the **RANGE END** mode to complete the task, when we don't want to scan a starting serial number in advance. The field _Serial numbers_ is empty - we can directly enter a value in the format ‘starting number ...  ending number’, where ‘ ... ‘ is a space, 3 dots and a space. 

1. Select the **RANGE END** mode;
2. Enter  ’XB0008 ... XB0012’ </br>

=>  the system will create 5 serial numbers - XB0008, XB0009, XB0010, XB0011 and XB0012.

## Mode selection
 
The **RANGE END of Serial numbers (from ... to)** mode can be selected:

- **manually** from the dropdown list in the Barcode panel.  
- **manually** by entering the **fast command #RNGEND#** in the main field when the panel is operating in one of the serial number modes.
- **automatically** after the selection of the product through the [Main mode](https://docs.erp.net/winclient/introduction/barcode-commands/barcode-modes/main-mode.html) - 

as long as the _Use serial numbers_ option from the Barcode settings is activated **AND** the product ‘_Is serialized_’ **AND** the form type is ‘Receive’ (for more information, see ‘Form types and mode selection’ in **[Barcode commands](https://docs.erp.net/winclient/introduction/barcode-commands/index.html)**) 

**AND:**

-it is the first use of the panel after opening the form **AND** the current mode is selected in the field _Default mode for serial numbers input_ from the Barcode panel settings 
 
**OR**

-it is **NOT** the first use of the panel after opening the form **AND** the current mode is the last mode used for serial numbers input.

- **automatically** after the selection of the starting serial number through the **[RANGE START](https://docs.erp.net/winclient/introduction/barcode-commands/barcode-modes/range-start.html)** mode.

## Mode operation

If **RANGE END** mode is set, when scanning/adding a value in the main field, the following actions are completed by the system:
 
**(1)** If the form type is different from "Receive" - throw **Message1** and return to the previous mode. Else => **(2)**
 
**(2)** Check if the field _Serial numbers_ has a value. If true => **(3)** Else => **(4)**
 
> [!NOTE]
> 
> If the field _Serial Numbers_ has a value, then this value is considered the "starting serial number" that has already been entered manually or through the **[RANGE START](https://docs.erp.net/winclient/introduction/barcode-commands/barcode-modes/range-start.html)** mode. 
 
**(3)** Check whether the scanned text is in the format "starting number ...  ending number". If false - throw **Message2** and clear the scanned text. Wait for another serial number => **(2)**. Else => **(4)**
 
**(4)** Check whether the prefixes of the starting and the ending numbers match. If false - throw **Message3** and clear the scanned text. Wait for another serial number => **(2)**. Else => **(5)**
 
**(5)** Check whether between the starting number (in _Serial Numbers_) and the final number there are more than 1,000 serial numbers. If true - throw **Message4** and clear the scanned text. Wait for another serial number => **(2)**. Else => **(6)**
 
**(6)** Add the scanned text to the text of the field _Serial Numbers_.
 
**(7)** Create a count of serial numbers – from the initial to the final. It is possible some serial numbers exist, but this fact won’t interfere with the process.
 
**(8)** Add new lines using current values of the fields in the panel.
 
**Message1**:<br>
The "{0}" mode is available only when all lines in the form are with the movement type "Receipt".
, {0} - ModeName
 
**Message2**:<br>
Invalid serial number range. The range should be in the format: START_NUMBER ... END_NUMBER
 
**Message3**:<br>
Invalid serial number range. The non-digit prefixes of the start number and the end number are different.

**Message4**:<br>
Invalid serial number range. The range exceeds 1000 elements.


