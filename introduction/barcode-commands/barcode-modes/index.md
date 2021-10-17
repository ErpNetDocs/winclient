# Barcode panel modes


The barcode panel supports several modes of operation:
- **[Main (barcode/command/name) mode](https://docs.erp.net/winclient/introduction/barcode-commands/barcode-modes/main-mode.html)** - selection of a product and a quantity.
- **[Lot number mode](https://docs.erp.net/winclient/introduction/barcode-commands/barcode-modes/lot-number.html)** - selection of a lot.
- **[Serial number mode](https://docs.erp.net/winclient/introduction/barcode-commands/barcode-modes/serial-number-mode.html)** - selection of a single serial number.
- **[LIST of serial numbers](https://docs.erp.net/winclient/introduction/barcode-commands/barcode-modes/list-numbers.html)** - quick scan of several serial numbers. 
- **[RANGE START of Serial numbers (from ... to)](https://docs.erp.net/winclient/introduction/barcode-commands/barcode-modes/range-start.html)** - selection of a starting serial number when creating a range of serial numbers.
- **[RANGE END of Serial numbers (from ... to)](https://docs.erp.net/winclient/introduction/barcode-commands/barcode-modes/range-end.html)** - selection of an ending serial number when creating a range of serial numbers.
- **[SEQUENCE START of Serial numbers (from ... count)](https://docs.erp.net/winclient/introduction/barcode-commands/barcode-modes/sequence-start.html)** - selection of a starting serial number when creating a sequence of serial numbers.
- **[SEQUENCE END of Serial numbers (from ... count)](https://docs.erp.net/winclient/introduction/barcode-commands/barcode-modes/sequence-end.html)** - selection of a count of numbers when creating a sequence of serial numbers. 
 
> [!**NOTE**]: Please, note that there is a separate subtopic for each mode which gives more details about its usage and operation.

## Form types and Mode selection 
 
Some of the modes are available only when the current form is in a specific type (see section **[Barcode panel modes](https://docs.erp.net/winclient/introduction/barcode-commands/barcode-modes/index.html)** above). There are three types – ‘Receive’, ‘Issue or ‘Indefinite’. The current form type could be seen after refreshing the ‘Movement Type’ button in the *Barcode tab*.

Generally, the form types are defined by whether all lines in the main lines panel are for receiving goods, for issuing goods or for both. Usually, the direction of the document forms is pretty clear. *Sales orders* , for example, are ‘Issue’ type forms and *purchase orders* are ‘Receive’ type forms. The situation is a bit more complicated when the form is actually a navigator, such as *Execute store orders*. This navigator could contains both ‘Receive’ and ‘Issue’ lines. In those cases the form type depends on the filtering. If the we have applied such filters that in the navigator lines there are only lines with a ‘Receipt’ direction , then the form type is ‘Receive’ and vice versa. If in the navigator are loaded lines with both direction the form type is ‘Indefinite’.
 
Barcode modes can be selected:
- **manually**  - the user can switch between the different modes from the drop-down list in the main field of the panel.
- **automatically** - for the Serial number modes there is also an automatic switching between modes. The switching is activated as the selection of the product is mostly influenced by the value of the ‘Default mode for serial numbers input’ field in the Barcode panel settings. For more information about the automatic switching between modes, please see the topic of the particular mode.
- by entering the **fast command** - the modes for a single serial number, list, range or a sequence of serial numbers could also be selected by using a fast command. The commands can be added manually or scanned from the command list. For more information about the available fast commands, please see **[Fast barcode panel commands](https://docs.erp.net/winclient/introduction/barcode-commands/fast-commands.html)**.

