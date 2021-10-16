# Main (barcode/command/name) mode

When the Main (Barcode/command/name) mode is set, when scanning/adding a code in the main field, the following actions are completed:

**(1)** Look for a product that relates to the particular code. If there is only one product, and it meets the conditions =>**(4)**

**(2)** Open a drop-down list in the field Product containing the products filtered by the scanned code. The system suggests the user to choose a product. Once a specific product is selected => **(4)**

**(3)** STOP

**(4)** A specific product has been selected. Check whether the product uses lots. If yes =>** (8)**

**(5)** Check whether the product uses serial numbers. If yes => **(10)**

**(6)** The product does not use lots or serial numbers. Add the record to the form:

A new line using current values of the fields in the panel is created (for example Quantity = 5 Product = XXX).

>[**!NOTE**]: When adding a new product line, then the panel is ‘cleared’ and ready to be >used again. The mode is ‘Main’.

**(7)** STOP

**(8)** Turn on ‘Lot’ mode.

**(9)** STOP

**(10)** Switch to the last chosen mode for serial numbers. If not (it is the first use of the panel after the opening of the form)  – the mode is chosen according to the following algorithm:

**(11)** If the type of the current form = ‘Receive’, the enabled mode will be mode which is selected in the field ‘Default mode for serial numbers input’ in the Barcode panel settings 

**(12)** If the type of the current form = ‘Issue’ or ‘Indefinite’, ‘, the enabled mode will be ‘Serial number.’

**(13)** STOP

