# ESP Homework

## Customer Orders View

### 0NF - List All Attributes

**Order:** Customer Name, Customer Number, <b class="pk">Order Number</b>, Order Date, Order Total, Payment Date, Payement Amount, Payment Number, Balance Owing, Payement Type, Deposit Batch Number.

### 1NF - Identify Repeating Groups

No Changes

### 2NF - Partial Dependancies

**Order:** <b class="pk">Order Number</b>, Customer Name, Customer Number, Order Date, Order Total

**Payment Details:** <b class="pk">Payment number</b>,<u class="fk">Order Number</u>, Payment Date, Payment Amount, Payment Number, Balance Owing, Payment Type, Deposit Batch #.

### 3NF - Transitive Dependancies

**Order:** <b class="pk">Order Number</b>, <u class="fk">Customer Number</u>, Order Date, Order Total

**Payment Details:** <b class="pk">Payment number</b>,<u class="fk">Order Number</u>, Payment Date, Payment Amount, Payment Number, Balance Owing, Payment Type, Deposit Batch #.

**Customer:** <b class="pk">Customer Number</b>, Customer Name.

### Summary

A customer may place one or many orders.

Each order must belong to one and only one customer.

Each customer may pay one or many payments.

Each payment must belong to one and only one customer.

Every payment must belong to one and only one order.

Every order may have one or many payments.

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