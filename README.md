# VincentMobile_Database_System
Vincent Mobile would like to develop a system that allows members to purchase the latest
mobile phone and tablets online while facilitating the trade-in service offline.
With the three main actors identified during the analysis phase, the system should consist of 3
modules for (1) customers and members, (2) administrators and managers, and (3) officers.
Through the system, administrators maintain the product list, such as introducing new products
and fading out obsolete products and update inventories when there are stock replenishments.
A customer registers as a member before making any purchases. After registering as member,
he/she searches for a list of products available for sale using keywords. After viewing the
product details, he/she may store desired products into a shopping cart datastore. Specifically,
the company maintains a shopping cart table which stores the shopping cart items for all
members. Individual member can view his/her own shopping cart items until they are
purchased. When a member views the shopping cart, the system should hide the out-of-stock
products to mitigate the risk of buying unavailable products. However, the shopping cart item
should be displayed again when the product is replenished.
A member may make a purchase with multiple products. He/she verifies the products to
purchase before completing the purchase. Member then enter a credit card number, the card’s
expiry date and CVC code to proceed. The system should also ensure that only available
products can be purchased.
For an order that does not require trade-in services, administrator can process the delivery
directly. Administrator reviews the list of confirmed orders from the system and informs the
warehouse to prepare for shipment, while the shipment preparation is not part of the system
scope. Upon informing the warehouse about the shipment through email or any other means,
administrator updates the status to “To be delivered”. Administrator then receives notifications
from the warehouse when the orders are delivered and updates the status of those orders to
“Completed”.
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
