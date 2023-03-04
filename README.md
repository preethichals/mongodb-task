# mongodb-task-02


Find all the information about each products

db.product.find().pretty()

Find the product price which are between 400 to 800

db.product.find({product_price: {$gte: 400,$lte: 800}})

Find the product price which are not between 400 to 600

db.product.find({product_price: {$lt:400, $gt:600}})

List the four product which are grater than 500 in price 

db.posts.find().sort({ product_name:1, product_price: {$gt:500  }).limit(4).pretty()

Find the product name and product material of each products

db.product.find({}, {product_name: 1, product_material: 1})

Find the product with a row id of 10

db.product.find({id:"1"})

Find only the product name and product material

db.product.find({product_name: 1, product_material: 1})

Find all products which contain the value of soft in product material 

db.product.find({product_material : {$regex : "soft"}}).pretty()

Find products which contain product color indigo  and product price 492.00

db.product.find({product_material : {$regex : "soft"}, product_price: "492"})

Delete the products which product price value are same

db.product.ensureIndex({product_price: 1}, {unique: true, dropDups: true})

