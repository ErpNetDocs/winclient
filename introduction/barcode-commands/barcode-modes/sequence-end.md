# SEQUENCE END of Serial numbers (from ... count)


## About the mode

This mode is introduced in Version 2019.1. It is used for **entering a count of numbers** when a sequence of an exact count of serial numbers starting from a particular number (for entering a start serial number use mode  **[SEQUENCE START of Serial numbers (from ... count)](https://docs.erp.net/winclient/introduction/barcode-commands/barcode-modes/sequence-start.html)** is created.

***Example:*** We want to create 5 serial numbers starting from serial number ‘XB0008’. In this case we could:

**[!NOTE]:** The product has already been selected manually or through the **[Main (barcode/command/name) mode](https://docs.erp.net/winclient/introduction/barcode-commands/barcode-modes/main-mode.html)**.

**Method 1:**

1. Select the **[SEQUENCE START of Serial numbers (from ... count)](https://docs.erp.net/winclient/introduction/barcode-commands/barcode-modes/sequence-start.html)** mode and enter the starting number ’XB0008’.
2. The system automatically switches to the current mode ‘SEQUENCE END of Serial numbers (from ... count)’ - enter ‘5’</br>
=> the system will create 5 serial numbers - XB0008, XB0009, XB0010, XB0011 and XB0012.

**Method 2:** Alternatively, we can use only the current ‘SEQUENCE END of Serial numbers (from ... count)’ mode to complete the task. This is when we don't want to scan a starting serial number in advance a.k.a the field ’Serial numbers’ is empty - we can directly enter a value in the format ‘starting number ...  count of numbers’, where ‘ ... ‘ is a space, 3 dots and a space. 
1. Select the **’SEQUENCE END of Serial numbers (from ... count)’** mode;
2. Enter  ’XB0008 ... 5’,</br>
=>  the system will create 5 serial numbers - XB0008, XB0009, XB0010, XB0011 and XB0012.

## Mode selection

The **‘SEQUENCE END of Serial numbers (from ... count)’** mode can be selected:
- **manually** from the drop down list in the Barcode panel.  
- **manually** by entering the **fast command #SEQEND#**  in the main field when the panel is operating in one of the serial number modes.
- **automatically** after the selection of the product through the **[Main (barcode/command/name) mode](https://docs.erp.net/winclient/introduction/barcode-commands/barcode-modes/main-mode.html)** - 

if the ‘Use serial numbers’ option in the Barcode settings is activated **AND** the products ‘Is serialized’ **AND** the form type is ‘Receive’ (for more information see ‘Form types and Mode selection’ section in topic **[Barcode commands](https://docs.erp.net/winclient/introduction/barcode-commands/index.html)**) **AND**:
  
  -it is the first use of the panel after opening the form **AND** the current mode is selected in the field ‘Default mode for serial numbers input’ in the Barcode panel settings 

**OR**

  -it is **NOT** the first use of the panel after opening the form **AND** the current mode is the last used mode for serial numbers input.

- **automatically** after the selection of the starting serial number through the **[SEQUENCE START of Serial numbers (from ... count)](https://docs.erp.net/winclient/introduction/barcode-commands/barcode-modes/sequence-start.html)**.

## Mode operation

If ‘SEQUENCE END of Serial numbers (from ... count)’ mode is set, **when scanning/adding** a value in the main field the following actions are **completed by the system**:

**(1)** If the form type is different from ‘Receive’ - throw **Message1** and return to the previous mode.  Else =>**(2)**

**(2)**  Check if the field ’Serial numbers’ has a value. If true => **(3)** Else => **(4)**

**Note:** If the field ’Serial numbers’ has a value, then this value is considered as the ‘starting serial number’ that has already been entered manually or through the **[SEQUENCE START of Serial numbers (from ... count)](https://docs.erp.net/winclient/introduction/barcode-commands/barcode-modes/sequence-start.html)** mode. 

**(3)** Check whether the scanned text is in the format ‘starting number ...  count of numbers’. If false - throw **Message2** and clear the scanned text. Wait for another serial number => **(2)**. Else =>**(4)**

**(4)** Check whether the entered value is a number between 1 and 1000. If false – throw  **Message3** and clear the scanned text. Wait for another serial number => **(2)**. Else => **(5)**

**(5)** Add the scanned/added serial number to the text of the field ‘Serial numbers’.

**(6)** Create count of serial numbers – from the initial number to the final number. It is possible that some of the serial numbers exist, but this fact won’t interfere with the process.

**(7)** Add new lines using current values of the fields in the panel.

**Message1:**

The ‘{0}’ mode is available only when all lines in the form are with movement type ‘Receipt’.</br>
{0} – ModeName

**Message2:**

Invalid serial number sequence. The sequence should be in the format: START_NUMBER ... COUNT

**Message3:**

Invalid count of elements in the serial number sequence. Please enter a number between 1 and 1000.

