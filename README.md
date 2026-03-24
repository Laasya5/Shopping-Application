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
3.Product service -- Customer(Searching by product name)[Filter in UI (sorting)]
4.Cart service -- add to cart, remove from cart(all, one item), showing cart
5.order service -- order placing,order cancelling, showing orders Admin(showing orders by userid)
6.payment -- paying, refunding
7.shipment -- kafka --showing shipment status , updating shipment status
8.inventory -- Admin(post products, update product availability, searching)
9.api gateway
10.config server
11.eureka server

Entities
1.Users(userid, usrname, pwd,email,role,created on)
2.Products(productId,name,category,price,availability,description,image,discount,rating)
3.Orders(orderid,userid,total,status,paymentid,shipmentid)
4.Order Items(id,orderid,productid,quantity,eachprice,totalprice)
5.Inventory(inventoryid,productid,availability)
6.Payments(paymentid, orderid, amount, payment method, status, transaction id, date)_
7.Notifications(id,userid,msg,type,status)
8.SHipment(shipmentid,orderid, shipmnet partner,tracking num,status,expected delivery date,delivered date)
9.Cart(id,cartid,productid,quantity)

![ER Diagram](https://github.com/user-attachments/assets/52f22c83-4a86-411d-a135-65ad8587b311)

LOGIN SERVICE
-rbac
-spring security
-jwt
-oauth

ADMIN SERVICE
-Controls users,products,orders
-rbac
-feign client(user ser,prod ser,order ser,inventory ser)

PRODUCT SERVICE
-Availability---Inventory(Kafkac) 
-rbac
-search n sort n filter


CART SERVICE
-feign client(prod service,order)
-jwt token validation for each user
-redis
-rbac

ORDER SERVICE
-redis

PAYMENT SERVICE

SHIPMENT SERVICE

INVENTORY SERVICE
-rbac
