https://karyab-api.herokuapp.com/register
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

 https://karyab-api.herokuapp.com/products
{
	"name": "mashin",
	"price":100,
	"modelYear":1398,
	"imageUrl":"C:a.jpg",
	"CategoryId":2,
	"BrandId":1
}
Post: add product
Get: get all products

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

https://karyab-api.herokuapp.com/comments
{
  "productId":"1",
  "comment":"my comment"
}
Post: add comment from current user to product 

http://localhost:8081/comments?productId=1
Get: Shows all comments that belongs to prduct with productId=1