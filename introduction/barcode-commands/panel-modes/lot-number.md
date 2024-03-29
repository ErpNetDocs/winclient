# Lot number mode

If this mode is set, when scanning/adding a lot number in the main field, the following actions are completed:

**(1)** Look for the lots related to the product set in the field _Product_. If there is only one lot related to this product => **(5)** </br>

**(2)** More than one lot meets the conditions. Open a dropdown list in the field _Lot_. The system recommends the user to choose a lot. Once a specific lot is selected=> **(5)**</br>

**(3)** There is no lot that meets the criteria. Clear the panel - the panel is ready to be used again.

**(4)** STOP

**(5)** Fill in the selected lot in the field _Lot_.

**(6)** Check whether the product uses serial numbers. If yes => **(10)**

**(7)** The product does not use a lot or a serial number. Create a new line using the current values of the fields in the panel.

**(8)** Switch to the last chosen mode for serial numbers. If not – the mode is chosen according to the following algorithm:

**(9)** If the type of the current form = ‘Receive’, the enabled mode will be the mode selected in the field _Default mode for serial numbers input_ from the Barcode panel settings.

**(10)** If the type of the current form = ‘Issue’ or ‘Indefinite’, then the enabled mode is **[Serial number](serial-number-mode.md)**.

**(11)** STOP.

