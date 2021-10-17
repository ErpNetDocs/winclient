# Fast barcode panel commands

For convenience, there is a predefined Command list with the ‘easy access’ commands that are recognized by the barcode panel. **The full list is available in the @@name client through the Command list button in the Barcode tab**. The list contains fast command codes/strings and their corresponding barcode labels i.e. the commands can be entered manually or scanned from the barcode labels. The list can be printed and attached to the working area, so it can be easily accessible during daily work with the barcode scanner.

The list contains commands allowing to add specific quantity for a product, entering a line, changing the serial number modes in the panel and oth.
 
##List of fast commands
 
### Quantity commands:**
- *- Resets the entered quantity.
- q*, where ‘q’ is a number i.e. 1, 10, 50, 500..:</br>
-Adds the entered number (q) to the current value of the Barcode panel’s quantity field.</br>
-When scanned in combination of a product code (q*productCode) – adds a new line with the entered product and Quantity equal to entered number(q).</br>
 
 
>**[!Note:]**The barcodes for some of the most frequenty used quantities are available in >the predefined list that can be downloaded form the Command list button in the Barcode 
>tab @@name client. If the desired quantity is present in this list, then it can be directly >scanned. Otherwise, it must be marked as the sum of existing quantities. For this purpose, >thequantities are sequentially scanned until the desired number is reached.
 

 ***Example:*** We want to execute 52 PCS of product code ‘0001’.
 
 
**Method 1**: We can scan the product label and consequently the quantity barcodes from the Command list  for ‘50*’ and end then for ‘2*’. The final quantity is 50 + 2, which is exactly 52;</br>

**Method 2:** We can scan the product label and then enter manually the command ‘52*’.</br>

**Method 3:** We can enter manually the command ‘52*0001’</br>


 
### Operational commands:

- #ADD# - Adds the data entered in the barcode panel as a new line e.g. new document line, input data line, etc.
- #CLEAR# - Clears all value from the fields in the barcode panel.
- #SKIP# - Skips the entering of lot or serial number and adds the data entered in the barcode panel as a new line.
- #UNDO# - Deletes the last line (new document line, input data line, etc.) created through the barcode panel.
- #FINISH# - Completes the data entering and creates a new document. It is available only for functional navigators.
 

### Serial number commands:
 
- #SERIAL# - Switches to Serial number mode for entering a single serial number. For more information about the mode, see **[Serial number mode](https://docs.erp.net/winclient/introduction/barcode-commands/barcode-modes/serial-number-mode.html)**.
- #LIST# - Switches to LIST of Serial mumbers mode used for entering serial numbers until the # ADD # command is executed. For more information about the mode, see **[LIST of Serial numbers (Finally - Scan # ADD #)](https://docs.erp.net/winclient/introduction/barcode-commands/barcode-modes/list-numbers.html)**.
- #RNGSTART# - Switches to RANGE START of Serial numbers (from ... to) mode for entering of the starting serial number when creating a range of serial numbers. For more information about the mode, see **[RANGE START of Serial numbers (from ... to)](https://docs.erp.net/winclient/introduction/barcode-commands/barcode-modes/range-start.html)**.
- #RNGEND# - Switches to RANGE END of Serial numbers (from ... to) mode for the ending serial number when creating a range of serial numbers. For more information about the mode, see **[RANGE END of Serial numbers (from ... to)](https://docs.erp.net/winclient/introduction/barcode-commands/barcode-modes/range-end.html)**.
- #SEQSTART# - Switches to SEQUENCE START of Serial numbers (from ... count) mode used for entering of the starting serial number when creating a sequence of serial numbers. For more information about the mode, see **[SEQUENCE START of Serial numbers (from ... count)](https://docs.erp.net/winclient/introduction/barcode-commands/barcode-modes/sequence-start.html)**.
- #SEQEND# - Switches to SEQUENCE END of Serial numbers (from ... count) Mode for entering of the count of numbers when creating a sequence of serial numbers. For more information about the mode, see **[SEQUENCE END of Serial numbers (from ... count)](https://docs.erp.net/winclient/introduction/barcode-commands/barcode-modes/sequence-end.html)**.

