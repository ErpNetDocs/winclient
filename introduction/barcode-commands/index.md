# Barcode commands


A barcode label is a special symbol to represent human readable information such as a product number or a lot number in machine readable format. In @@name barcode labels could be used through the Barcode commands panel. This panel allows very quick and operational work with barcode labels via barcode reader in the forms containing product lines. The product can be added in the lines by using their product name, part number or a product code (using Coding systems). Information such as *quantity*, *lot*or *the serial number* cab also be inputted.

## The barcode tab

The Barcode tab is accessible only if the Barcode commands panel is visible in the view. It contains several buttons which redound to the work of the panel, but it also contains a *Settings button*. When pressed, it opens the *Settings window* where we can edit the list of the barcode command handlers with different options (such as ‘Use lots’, for example) which are or can be activated. 

>**[!Note:]** It is very important to remember that the Barcode Settings are individually set >for each View (the selected options are saved in the View).

There also is a *Command list* button for convenience, loading the list with the ‘easy access’ commands that are recognized by the panel. For more information, see **[Fast barcode panel commands](https://docs.erp.net/winclient/introduction/barcode-commands/fast-commands.html)**.

## Barcode commands handlers

Different barcode command handlers by which the information from the barcode label is recognized can be activated from the Barcode Settings in the *Barcode tab*. Currently, there are three types of handlers – **General (quantity, product name…)**, **Other **([GS1-128 Barcode command handler](https://docs.erp.net/winclient/introduction/barcode-commands/barcode-handler.html)**, **Mettler Toledo / EAN-13 BPRO)** and **Coding systems** (user defined). The barcode commands are handled only by the active command handlers in the specified order. The active command handler list can be reordered by using *Drag and Drop*.

## Barcode panel options

 Two additional options can also be activated in the barcode setting in the *Barcode tab* – **Use lots** and **Use serial numbers**.
- If ‘Use lots’ is on, when the system recognizes the product (if the product is allowed or required to use lots), it does not create a line immediately, but changes the barcode panel mode and waits until information  about the lot number is received. The lot number can be added via barcode label, manually in the main field or from the drop-down list in the lot field.
- If ‘Use serial numbers’ is on, when the system recognizes the product (if the product is serialized), it does not create a line immediately, but changes the barcode panel mode and waits until information about the serial number is received. The lot number can be added via barcode label and manually in the main field or in the serial number field.

## Barcode panel modes

The barcode panel supports multiple modes which allow entering quantities, lots and serial numbers. For more information, see **[Barcode panel modes](https://docs.erp.net/winclient/introduction/barcode-commands/barcode-modes/index.html).**


