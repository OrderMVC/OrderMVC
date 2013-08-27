/ - index
---------

Asks user for stored name for new orders or shows name (with ability to change name).
Link to "Shop" - "/items"
Link to "View Orders" - "/orders"

/items - items.index
----------------------

Shows all DigitalItems and PhysicalItems in a grid
Link to "Add Item to Cart" - ":type/:id/add"
Link to "Update Item" - ":type/:id/edit"
Link to "View Cart" - "/cart"
Link to "Add Item" - "/items/new"
Link to "Checkout" - "/orders/new"

/items/new - items.create
----------------------

Link to "Create Digital Item" - "digital_items/new"
Link to "Create Physical Item" - "physical_items/new"
Link to "Back" - Force Back

/digital_items/new - digital-items.create
----------------------

Inputs - name, size, format, price
Submit POST - "/digital_items"

POST /digital_items - digital-items.store
----------------------

Creates new DigitalItem
Redirects to - "/items"

/physical_items/new - physical-items.create
----------------------

Inputs - name, weight, stock, price
Submit POST - "/physical_items"

POST /physical_items - physical-items.store
----------------------

Creates new PhysicalItem
Redirects to - "/items"

/cart - cart.index
----------------------

Shows all items in cart
Shows total
User can update number of items - POST "/cart"
User can remove items from cart - ":type/:id/remove"
Link to "Checkout" - "/orders/new"

/orders - orders.index
----------------------

Shows all orders in table
Link to "Order Details" - "/orders/:id"
Link to "Delete Order" - DELETE "/orders/:id"

/orders/:id - orders.show
----------------------

Shows all items in cart
Shows total
Shows address
Link to "Back" - Force Back

/orders/new - orders.create
----------------------

Shows all items in cart
Shows total
Link to "Update Cart" - "/cart"
Inputs - address.street, address.city, address.state, address.zip
POST /orders - orders.store
Link to "Back" - Force Back

POST /orders - orders.store
----------------------

Creates order from items in cart and address inputs and Customer Name