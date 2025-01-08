---
uid: spec-PoFD
items: Specific-functionality
---
# Print Receipt and issue Invoice

In Sales and Payments, there is a 'Fiscal Printer Print' panel that enables the fiscalization of sales and payments. The panel contains two buttons:

Receipt (F7) - which prints a fiscal receipt on the fiscal device.
Invoice + Receipt - which allows for easy issuance of an invoice for the current sale. It appears in the panel only when it is for a sale.

The button Invoice + Receipt operates in several ways:

If a receipt has not yet been printed, the receipt is first printed and then the invoice is created and displayed on the screen.
If the receipt has already been printed, it simply creates the invoice and displays it on the screen.
If an invoice already exists or more than 5 days have passed since the receipt was printed, the button is inactive.

The button's functionality heavily depends on the configuration of the  document flow. It is expected that there will be a planned store order  in the flow, which is released first. Afterward, a invoicing order with a configured manual document route for invoice creation is sought out.

![image-20231006155529750](image-20231006155529750.png)



```

```


The Invoice button performs the following actions:

1. Release the Store Order

2. Generates an Invoice from the created Invoice Order, using the configured manual generation

3. Opens the generated invoice on the screen

   

Prerequisites:

1. When the Sales Order is released, a Store Order with the status "Planned" and Invoice Order with the status "Released" are generated.

2. When the Store Order is released, a released Store transaction is generated.

3. The Invoice Order has a document workflow configured on status "Released" for the manual generation of an Invoice with the status "Planned."

   ![image-20240705154930313](pictures/print-on-fiscal-device/image-20240705154930313.png)

   ![image-20240705155204639](pictures/print-on-fiscal-device/image-20240705155204639.png)

   ![image-20240705155307214](pictures/print-on-fiscal-device/image-20240705155307214.png)

   

   

   

   

