# Create a copy of a product


**Create a copy** is a function that is available in the **Functions** tab (product's definition). This function allows us to create a new product from the current one. Note that not all data from the base product is copied to the new one. 

The tables currently copied to the new product are: 

- **Identification** - only product name is copied. The description is not copied and the part number is inherited by the value of the field _Next Part Number_ of the product group.
- **Data**
- **Product dimensions**
- **Variants**
- **Document amounts**
- **Default store bins for products**
- **Custom properties**
- **Product pictures**
- **Product distribution channels**

The lots, serial numbers, product codes, prices, purchase prices and discounts are NOT copied to the new product.

> [!NOTE]
> 
> Some of the records of the copied panels (such as **Custom properties**) are loaded after the saving of the new product.

