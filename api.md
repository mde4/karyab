https://karyab-api.herokuapp.com/register
{
  "email":"e@m.ail",
  "password":"12345678",
	"name":"amirReza"
}

https://karyab-api.herokuapp.com/login
{
  "email":"e@m.ail",
  "password":"12345678"
}

https://karyab-api.herokuapp.com/brands
{
	"name": "LG"
}
Post: add brand
Get: get all brands

 https://karyab-api.herokuapp.com/categories
{
	"name": "Sports"
}
/Post: add category
Get: get all categories

 https://karyab-api.herokuapp.com/products?page=0&pageSize=5&search=good
{
	"name": "mashin",
	"price":100,
	"modelYear":1398,
	"imageUrl":"C:a.jpg",
	"CategoryId":2,
	"BrandId":1
}
Post: add product
Put: edit product
Get: get all products

https://karyab-api.herokuapp.com/products?categoryId=1&storeId=3&page=0&pageSize=5
get: if categoryId is set => show chats of categoryId 2

get: if storeId is set => show chats of storeId 3

https://karyab-api.herokuapp.com/products/1
Get: Show product with productId=1. 
if there is no such product=> status: 404, {"msg": "there is no such product"}

https://karyab-api.herokuapp.com/bookmarks
{
	"productId":2
}
Post: add Bookmark  from logged in user to product 2(Bearer Token needed)

https://karyab-api.herokuapp.com/bookmarks
Get: Show all products bookmarked by user (Bearer Token needed)

https://karyab-api.herokuapp.com/bookmarks?productId=3
Get:Shows if User bookmarked product with productId=3 (Bearer Token needed)

https://karyab-api.herokuapp.com/bookmarks/14
Delete: Deletes bookmark with Id number =14, if it belongs to current user

https://karyab-api.herokuapp.com/rateComments
{ "productId":1,"rate":5, "comment":"my comment3","storeId":1 }
Post: add comment & rate  from current user to product 

https://karyab-api.herokuapp.com/rateComments?productId=1
Get: Shows all comments and rates that belongs to prduct with productId=1

https://karyab-api.herokuapp.com/rateComments/1
Delete: delete comment sent from logged in user for product with productId=1


https://karyab-api.herokuapp.com/stores
{ 
	"name": "ssan",
	"phone": "87987587",
	"email": "abc@de.fgh",
	"address": "yazd",
	"postalCode": "8918889900"
	"UserId":1
}
Post: add store
Get: get all stores

https://karyab-api.herokuapp.com/stores/1
Get: Show store with storeId=1. 
if there is no such store=> status: 404, {"msg": "there is no such store"}

https://karyab-api.herokuapp.com/stocks
{"storeId":1, "productId":1, "quantity":4}
Post: add quantity to store inventory

https://karyab-api.herokuapp.com/stocks?storeId=1&productId=1
Get: returns quantity of product 1 in store 1

https://karyab-api.herokuapp.com/stocks?storeId=1
Get: returns all products of store 1

https://karyab-api.herokuapp.com/stocks?productId=1
Get: returns all stores that have product 1


https://karyab-api.herokuapp.com/shopping-cart/1/count/5
Get: set the value of product with id 1 to shopping cart to 5.
if there is no such product => status: 404, {"msg": "there is no such product"}

https://karyab-api.herokuapp.com/shopping-cart/remove/1
Delete: remove product with id 1 from shopping cart.

https://karyab-api.herokuapp.com/shopping-cart/
Get: shows the content of shopping cart.

https://karyab-api.herokuapp.com/checkout
{"name": "ali", "mobile": "09132525555", "province": "yazd", "city": "yazd", "address": "azadshahr", "postalCode": "9876543210"} 
Post: add user specification to shopping cart object

https://karyab-api.herokuapp.com/users/1
Get: shows the the user fields.

https://karyab-api.herokuapp.com/users
{
    "id": 1,
    "name": "ali",
    "phone": "09138765432",
    "address": "tehran",
		"role": "staff",
    "postalCode": "9876543210"
}
Put: change user fields with userId=1

https://karyab-api.herokuapp.com/provinces
Get: show provinces

https://karyab-api.herokuapp.com/provinces/31
Get: show the cities of province 31

https://karyab-api.herokuapp.com/provinces

https://karyab-api.herokuapp.com/chats
{ 
	"title":"title7",
	"productId":1,
	"storeId": 1,
	"message":"my new message1"
 }
 post : create chat about product 1 that belogns to store 1
 get : show all chats of current logged in user

https://karyab-api.herokuapp.com/chats/20
{ "message":"edited by owner of this message " }
put: edit chat with id 20 if it belongs to currently logged in user
delete: delete chat

https://karyab-api.herokuapp.com/chats?conversationId=2&productId=2&storeId=2
get: if conversationId is set => show chats of conversationId 2

get: if productId is set => show chats of productId 2

get: if storeId is set => show chats of storeId 2

 https://karyab-api.herokuapp.com/storeConversations
 {
	"conversationId": 9,
 	"message": "my response to conversation 69"
 }
 post: response to conversation that was created by a customer. 
 get: show conversations that belongs to currently logged in staff.
