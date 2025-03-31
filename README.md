# VincentMobile_Database_System

## Background

Vincent Mobile would like to develop a system that allows members to purchase the latest
mobile phones and tablets online while facilitating the offline trade-in service.

With the three main actors identified during the analysis phase, the system consists of 3
modules for:
1. customers and members
2. administrators and managers
3. officers

## Key functions

_Administrator_
- Maintain the product list, including introducing new products, fading out obsolete products, and updating inventories when there is stock replenishment.
- Reviews the list of confirmed orders from the system

_Customer_
- Register as a member before making any purchases
- Search for a list of products available for sale using keywords.
- View product details, and store desired products in a shopping cart datastore.
  
  Specifically, the company maintains a shopping cart table that stores the shopping cart items for all members. Individual members can view their shopping cart items until they are purchased. When a member views the shopping cart, the system should hide the out-of-stock products to mitigate the risk of buying unavailable products. However, the shopping cart item should be displayed again when the product is replenished.

- Purchase with multiple products
- Verify products to purchase before completing the purchase.
- Proceed Payment: Enter a credit card number, the card’s expiry date, and CVC code to proceed.

_Additional Requirements_
1. The system should also ensure that only available products can be purchased. For an order that does not require trade-in services, the administrator can process the delivery directly.
2. Upon informing the warehouse about the shipment through email or any other means, the administrator updates the status to “To be delivered”. The administrator then receives notifications from the warehouse when the orders are delivered and updates the status of those orders to “Completed”.
While member indicates old devices information for trade-in while making the purchase online,
he/she brings in the old devices to officer at the customer service point in person. Officer
retrieves the trade-in details from the system, inspects the device and give a trade-in offer.
Spring 2024-2025
Page 2 of 5
When member agrees with the trade-in offer, the order price will be adjusted according to the
agreed trade-in offer and before proceeding with the order shipment. Officer also updates the
information of the traded-in devices in the database.
However, when member rejects the trade-in offer, he/she has an option to proceed with the
order shipment as if no trade-in involved, or simply to cancel the order. Officer executes the
decision for the customer through the system. Member can trade in many old devices in one
order. However, the trade-in discount provided must not exceed the order amount.
Manager, a role done by the same group of administrators, generates numerous operational and
managerial reports to facilitate the company’s operations and development
