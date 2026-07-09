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

Upon acquiring customer approval or order confirmation, create the sales order via the submitted quotation. Then, determine the appropriate method to [communicate the sales order](../system-communications/system-communications.md#sales-order) to the customer based on their location and payment preference:

- **Out-of-state customers (Pre-payment required)**: Follow the instructions to send the sales order [with a payment link](../system-communications/system-communications.md#scenario-1-with-payment-link).
- **Local customers (Payment on delivery/pickup)**: If paying by check or credit card upon delivery, send the sales order [without a payment link](../system-communications/system-communications.md#scenario-2-without-payment-link-local-delivery-or-pickup) by replying to their existing email conversation with the PDF attached.

---
