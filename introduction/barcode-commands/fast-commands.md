# Fast barcode panel commands

For convenience, there is a predefined command list with ‘easy-access’ commands that are recognized by the **Barcode** panel. 

- The full list is available in the @@name client through the **Command list** button in the Barcode tab. 

- The list contains fast command codes/strings and their corresponding barcode labels i.e. the commands can be entered manually or scanned from the barcode labels.

- The list can be printed and attached to the working area, so it can be easily accessible during daily work with the barcode scanner.

- The list contains commands allowing to add specific quantity for a product, entering a line, changing the serial number modes in the panel, and others.
 
## List of fast commands
 
### Quantity commands:

- * /- resets the entered quantity.
- q*, where ‘q’ is a number i.e. 1, 10, 50, 500..:</br>

    - q* adds the entered number (q) to the current value of the **Barcode** panel’s *Quantity* field.</br>

    - When scanned in combination with a product code (q*productCode), it adds a new line with the entered product and quantity equal to entered number(q).</br>
 
 
>[!NOTE]
>
> The barcodes for some of the most frequently used quantities are available in the predefined list that can be downloaded from the **Command list** button in the barcode tab @@name Client. If the desired quantity is present in this list, then it can be directly scanned. Otherwise, it must be marked as the sum of existing quantities. For this purpose, the quantities are sequentially scanned until the desired number is reached.
 

 **Example:** We want to execute 52 PCS of product code ‘0001’.
 
 
**Method 1**: We can scan the product label and consequently the quantity barcodes from the command list for ‘50*’ and end then for ‘2*’. The final quantity is 50 + 2, which is exactly 52;</br>

**Method 2:** We can scan the product label and then manually enter the command ‘52*’.</br>

**Method 3:** We can manually enter the command ‘52*0001’</br>


 
### Operational commands:

- #ADD# - Adds the data entered in the Barcode panel as a new line e.g. new document line, input data line, etc.
- #CLEAR# - Clears all value from the fields in the Barcode panel.
- #SKIP# - Skips the entering of lot or serial number and adds the data entered in the Barcode panel as a new line.
- #UNDO# - Deletes the last line (new document line, input data line, etc.) created through the Barcode panel.
- #FINISH# - Completes the data entering and creates a new document. It is available only for functional navigators.
 

### Serial number commands:
 
- #SERIAL# - Switches to **[Serial number mode](panel-modes/serial-number-mode.md)** used for entering a single serial number.
- #LIST# - Switches to **[LIST of serial numbers mode](panel-modes/list-numbers.md)** used for entering serial numbers until the # ADD # command is executed.
- #RNGSTART# - Switches to **[RANGE START of serial numbers mode](panel-modes//range-start.md)** used for entering the starting serial number when creating a range of serial numbers.
- #RNGEND# - Switches to **[RANGE END of serial numbers mode](panel-modes//range-end.md)** used for entering the ending serial number when creating a range of serial numbers. 
- #SEQSTART# - Switches to **[SEQUENCE START of serial numbers mode](panel-modes//sequence-start.md)** used for entering the starting serial number when creating a sequence of serial numbers.
- #SEQEND# - Switches to **[SEQUENCE END of serial numbers mode](panel-modes//sequence-end.md)** used for entering of the count of numbers when creating a sequence of serial numbers.

