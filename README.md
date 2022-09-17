# Store API testing by using Postman + newman + github actions

## Steps to run

1. Download this repository and open it in IDE
2. Run in terminal `npm i` (install all dependencies)
3. Run in terminal `npm install -g newman` (install newman)
4. Run in terminal `npm run tern-on-api` in **Git bash** terminal (to run local server for api testing)

## Test execution
Run in terminal `newman run storenew.collection.json`(to run API tests)
**OR**
Import storenew.collection.json into Postman and run each test manually

### Overview of local server testing
Routes `/products`, `/orders` and `/users`. Below is a table of supported operations with `products` as example resource. The same operations are also supports for `orders/` and `users/`.

| VERB     |Route          | Input      | Output             |
|----------|---------------|------------|--------------------|
| GET      | /products     | *None*     | **Array**          |
| GET      | /products/:id |  **e.g 3** | **Object**         |
| POST     | /products     | **object** | **Created object** |
| PUT      | /products     | **object** | **Updated object** |
| DELETE   | /products/:id | **e.g 3**  | **Deleted object** |