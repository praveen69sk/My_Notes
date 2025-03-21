>Code Step by Step

>GUI tool 
  * --> MonogoDB Compass
  * --> Studio 3T (Earlier it was called as Robo 3T)

>Commands
* mongosh --> for command line
* show dbs

***
# Mongoose

```html

Mongoose is a MongoDB object modeling tool designed to work in an asynchronous environment. Mongoose supports Node.js and Deno (alpha).

```

> In Mongoose we can define data type and add restrictions using schemas

```js
import mongoose from "mongoose"

const main = async () =>{
    await mongoose.connect('mongodb://localhost:27017/e-comm');
    const ProductSchema = new mongoose.Schema({
        name: String,
        price: Number
    });

    const ProductsModel = mongoose.model('products', ProductSchema);
    let data = new ProductsModel({
        name: 'Praveen',
        price: 300000
    });
    let result = await data.save();
    console.warn(result);
}

main();
```