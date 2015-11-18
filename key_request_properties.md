# Key Request Properties

In the Taxify APIs, there are certain key properties for each request JSON call:
 
<DocumentKey>: A unique identifier of the transaction, i.e., invoice number. Please provide a configurable "prefix" to prevent overlap with other data sources which may be integrated to a Taxify account.

<IsCommited>: This should be set to "true" to indicate a complete transaction which should be included on state tax returns.

<ActualExtendedPrice>: The total price for the item to be charged to the customer (quantity * unit price). If any item level discounts are applied, they should be included in the ActualExtendedPrice.

<Quantity>: A quantity is required for each line, 0 quantity rows will be ignored, set to 1 if not available.

<ItemTaxability>:

(blank): Taxify will assume the item is generally taxable "tangible goods" unless otherwise configured (by ItemKey) in Taxify.

NON: A generally non-taxable item or service.

FR: Shipping - It is important to identify shipping charged using this tax code, as taxability of shipping differs state to state.

[custom] - Taxify can also handle hundreds of special taxability codes, however, often we recommend special taxability be managed in Taxify.

<CustomerTaxability>:

(blank): Used for a default, retail transaction.

RESALE: Used for a reseller/wholesale transaction - sales tax will not be charged (in general), but transaction may be reported (varies by state).

<DestinationAddress>:

Most fields are optional. <Region> (state code) or <PostalCode> (zip) are required. The more information that is provided, the higher the accuracy of tax jurisdiction determination/calculation.

Note: if all fields are left blank except <Street1>, Taxify will attempt to parse a complete/valid address.