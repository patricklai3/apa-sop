# Standard Sales Workflow

### Step 0: Identify Customer Type

When selecting a customer for a quotation, choose from one of the following scenarios:

- **Insurance**: For insurance companies asking for list prices.
- **New customer**: Use the `"shop"` profile for customers asking for prices when info cannot be quickly collected over the phone.
- **Existing customer**: Use their existing profile.

### Step 1: Provide Quotation

[Generate](../quotation/create_quotation.md) and provide a quotation to the customer.

- Learn [how to acquire an electronic form of the document](../system-communications/system-communications.md#quotation) to send to the customer.

> [!TIP]
> **Shortcut:** If an existing customer requests an order without a quotation, you can skip this step. Instead, [create a sales order](../sales-order/create_sales_order.md) directly and proceed to the next step.

### Step 2: Confirm, Create & Provide Sales Order

Upon acquiring customer approval or order confirmation, [create a sales order](../sales-order/create_sales_order.md) via the submitted quotation. Then, determine the appropriate method to [communicate the sales order](../system-communications/system-communications.md#sales-order) to the customer based on their location and payment preference:

- **Non-local customers (Pre-payment required)**: Follow the instructions to send the sales order [with a payment link](../system-communications/system-communications.md#scenario-1-with-payment-link).
- **Local customers (Payment on delivery/pickup)**: If paying by check or credit card upon delivery, send the sales order [without a payment link](../system-communications/system-communications.md#scenario-2-without-payment-link-local-delivery-or-pickup) by replying to their existing email conversation with the PDF attached.



## Non-Local Customer Procedures

This procedure outlines the process for handling non-local customers who require prepayment. Once payment is received, you will process the shipment and issue the final invoice.

### Step 3: Record Payment

Once payment is received via the payment link, [record payment](../payment/payment.md) through the respective sales order.

### Step 4: Pick Items

Print the Sales Order (SO) to use as a pick list. Record which warehouse the items were picked from.

### Step 5: Pack and Ship

Pack the shipment and create the applicable shipping label:

- **Scenario 1:** Create a [standard shipping](../package/package-shipping.md) label.
- **Scenario 2:** Create an [LTL shipping](../ltl/ltl.md) label.

### Step 6: Create Sales Invoice

Create a [Sales Invoice (SI)](../sales-invoice/invoice.md) from the Sales Order.

### Step 7: Send Sales Invoice and Tracking

Send the Sales Invoice, along with the tracking information, to the customer via the appropriate [invoice email version](../system-communications/system-communications.md#sales-invoice).

