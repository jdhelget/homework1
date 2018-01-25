# ESP 3 Specifications

## Customer Order View

### 0NF - List All Attributes

**Order:** <b class="pk">Purchase Order #</b>, Supplier Name, Address, City, Phone, Supplier Number, Date, Item #, Suppliers Item #, Suppliers Description, Quantity, Cost,Amount, SubTotal, GST, Total, <g class="gp">{</g>Current Sale Price, Item Description, Order Date, Supplier Number, PO Number, Quantity, Cost<g class="gp">}</g>

### 1NF - Identify Repeating Groups

**Order:** <b class="pk">Purchase Order #</b>, Supplier Name, Supplier Number, Address, City, Phone, Date, SubTotal, GST, Total, Current Sale Price, Item Description, <g class="gp">{</g>Order Date, Supplier Number, PO Number, Quantity, Cost<g class="gp">}</g>

**Order Details:** <b class="pk">Item #, Suppliers Item #,</b> Description, Quantity, Cost, Amount.


### 2NF - Partial Dependancies

**Order:** <b class="pk">Purchase Order #</b>, Supplier Name, Supplier Number, Address, City, Phone, Date, SubTotal, GST, Total

**Order Details:** <b class="pk"><f class="fk">Purchase Order #, Item #,</f></b> Suppliers Item #, Description, Quantity, Cost, Amount.

**Inventory:** <b class="pk">Item #,</b> Description, Order Date, Supplier #, PO #, Quantity, Cost, Current Sale Price.

### 3NF - Transitive Dependancies

**Order:** <b class="pk">Purchase Order #</b>, Date, SubTotal, GST, Total

**Order Details:** <b class="pk"><f class="fk">Purchase Order #, Item #,</f></b> Suppliers Item #, Description, Quantity, Cost, Amount.

**Inventory:** <b class="pk">Item #,</b> Description, Order Date, Supplier #, PO #, Quantity, Cost, Current Sale Price.

**Supplier:** <b class="pk">Supplier #,</b> Supplier Name, Address, City, Phone

 ----

<style type="text/css">
.pk {
    font-weight: bold;
    display: inline-block;
    border: solid thin blue;
    padding: 0 1px;
}
.fk {
    color: green;
    font-style: italic;
    text-decoration: wavy underline green;
}
.gp {
    color: darkorange;
    font-size: 1.2em;
    font-weight: bold;
}
</style>