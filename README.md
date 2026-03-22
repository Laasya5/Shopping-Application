# Shopping-Application

Users
1.Admin
2.Customer
3.Shipment Providers

Operations
1.Admin
-CRUD Inventory
-Manage Inventory
-View Orders

2.Customer
-SignUp/Login
-Add to Cart
-Place order
-Cancel order

3.Shipment Providers
-Receives shipment event after order placed by customer
-Updates status of shipment(Tracking)
-Delivery status

Services
1.Login service--Creating Users,login user,logout user
2.Admin -- managing users, update users, delete
3.Product service -- Admin(post products, update product availability, searching) Customer(Searching by product name)[Filter in UI (sorting)]
4.Cart service -- add to cart, remove from cart(all, one item), showing cart
5.order service -- order placing,order cancelling, showing orders Admin(showing orders by userid)
6.payment -- paying, refunding
7.shipment -- kafka --showing shipment status , updating shipment status
8.api gateway
9.config server
10.eureka server

Entities
1.User
2.Admin
3.
