# GS1-128 Barcode command handler

**GS1-128** is an application standard of the GS1 implementation using the code 128 barcode specification. In the past, GS1-128 was also known as UCC/EAN-128. **GS1-128** uses a list of different application identifiers (AI) in order to include additional data such as quantity, lot and serial numbers and many others.

In Version 2017, a new barcode command handler - GS1-128 is introduced. Based on the GS1-128 standard, it includes several of its application identifiers. In more detail, the AI recognised by GS1-128 handler are:

- (01) Global Trade Item Number (GTIN), (02) GTIN of Contained Trade Items, (10) Batch/Lot Number, (21) Serial Number, (37) Number of Units Contained. 

When used/ recognised, those identifiers input values in one of the following fields (Table1):
 
|Code|Description|Program field
|:--|:--|:--
|01| Global trade item number (GTIN)| 
|02| GTIN of contained trade items|Product
|10| Batch|Lot Number| Lot
|21| Serial number| Serial Number
|37| Number of units contained| Quantity (In the Quantity unit of the Coding system)

   *(Table1) List of application identifiers recognised by the GS1-128 handler*
 
The operation of the GS1-128 barcode commands handler is explained in the next steps, fully describing its working process.
 
- **Step 1**

The system attempts to split the scanned text into segments of the following format ‘(xxx ... x) yyy ... y’.  Where ‘xxx ... x’ would contain at least two characters (‘xxx ... x’ will be referred to in the text as ‘segment code’) and ‘yyy ... y’ is a non-empty text. Both ‘xxx ... x’ and ‘yyy ... y’ do not need to contain brackets ‘(‘ or ‘)’.

If the text cannot be separated into those segments, \the reading by the GS1-128 handler fails and the system does not continue the next steps.

**For  example**, the text (02)TEST00012479222(10)L00028(37)5 is split into segments (02)TEST00012479222, (10)L00028 и (37)5. In the first segment ‘xxx...x’ is ‘02’ and ‘ ‘yyy...y’ is TEST00012479222.. and so on.

For texts like 22503(01)54030893330, ()22503(01)54030893330, (01)805485305840)4584, (1)8HHJ4584(01)PRD442607224 or (02)453893890899(10), the reading fails.
 
- **Step 2**

From the segments which are a result of the previous step, only those with a segment code 01, 02, 10, 21 or 37 are taken into consideration. The remaining segments are neglected and do not participate in the next steps.

For example, if the text is (02)TEST00012479222(10)L00028(12)6646(21)KKE334(22)DW634(37)5(329y)798454, segments (02)TEST00012479222, (10)L00028 и (37)5 are going to be used in the next steps and segments (12)6646, (21)KKE334, (22)DW634 и (329y)798454 are going to be neglected.
 
- **Step 3**

Certain validations for compatibility between codes (xxx ... x s) of the segments are made in this step. If any of the validations finds that the text is invalid, then reading by the GS1-128 handler fails and the system does not continue the next steps.

Validations:</br>

- Each of the segment codes 01, 02, 10, 21 or 37 can be part of only one of the segments in the text. </br>

*For example*, texts like (02)HJ453494573945(37)12, (10)LОТ55490380934(21)455340300303 and </br>
(02)TEST00012479222(10)L00028(12)6646(21)KKE334(22)DW634(37)5(329y)798454 are valid commands, while </br>
(02)HJ453494573945(37)12(37)445(329y)798454 and (01)45373532234BBA98(01)YYE436373(10)LOT17 are not.

- The text needs to contain at least one segment with code 01 or 02.

*For example*, texts like (01)45373532234BBA98 and (02)HJ453494573945(37)12 are valid, while (10)LОТ55490380934(21)455340300303 is not.</br>

- The text does not have to contain segments with segment codes 01 and 02 simultaneously.</br>

*For example*, (01)45373532234BBA98 and (02)HJ453494573945(37)12 are valid texts, while (10)LОТ55490380934(21)455340300303 is not;

- If the text contains a segment with code 37, then it must also contain a segment with code 02.</br>

*For example*, (02)HJ453494573945(37)12 is a valid text, while (01)HJ453494573945(37)12 is not.
 
If any of the validations find that the text is invalid, then the reading by the GS1-128 handler fails and the system DOES not continue the next steps.
 
- **Step 4**

In step 4, the recognition of products and/or lots, serial numbers and quantities through the ‘yyy ... y’ parts of the segments is performed.

First, the system finds the part ‘yyy ... y’ of the segment with one of the following codes 01 or 02 (whichever is available in the text). For this value, the system searches for a product, as it usually does when a barcode panel is used. If it finds such a product – a new record with the recognised product is created in the input data table. The input data table contains the records according to which the lines of the document/report are going to be created after performing the operation.

If the text contains a segment with code 10, its ‘yyy ... y’ part is used for the recognition of a lot (as standardly done in the barcode panel). If the system finds such a lot, it is saved in the already generated record in the lines of the document/ report (if the record in the input data table was not created after the search for the product – it is created now).

The same happens with a segment with code 21 – through its ‘yyy ... y’ part the system searches for a serial number and if such is found, it needs to be inputted in the record (if the record in the input data table was not created after the search for the product – it is created now).

And if there is a segment with a code 37, its ‘yyy ... y’ part is converted to a positive integer. If this is possible, the value is inputted in the field Quantity of the generated record. The system searches for the coding system with which the record is added and also inputs its default unit in the Quantity unit field (if the record in the input data table was not created after the search for the product – it is created now).
 
If the ‘GS1-128’ handler has failed during some of the steps, then the system proceeds to the next handler of the list (the whole text is transmitted to the next handler).

If ‘GS1-128’ did not fail and the product, the lot, the serial number and the quantity are successfully retrieved (filled in the input record), the system does nothing much. i.e. does not proceed to subsequent handlers in the list.

And if any of the product, lot, serial number or quantity is not extracted (for example, because a product with this barcode/part number is not found in the base), then the system proceeds to the following handles which can be able to fill in the empty values. 

