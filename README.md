# note-taker
Leverage Restful API endpoints to interact with an ecommerce backend database containing categories, products and tags.

## Description
The ecomm-backend connects to an existing mySQL database. There are individual API endpoints to get all Categories and to get a single Category by ID. Additionally similar endpoints exist for products and tags. 

Put, post and delete API endpoints have also been created to allow the category, products and tags to be created, updated and deleted through the API.

This project relied on the following technologies:
- Express routes for GET, POST and DELETE API requests
- JS Models and Sequelize for the creation of Categories, Products and Tags as well as the relationship connection
- dotenv for storing and protecting environmental database information
- insomnia for enpoint testing

## Installation
N/A

## Usage

A testing video can be found here : [here](https://drive.google.com/file/d/1Is0ujlNiJxnf0ZlUYX1TLLc9MRV-fBxM/view)
- The testing vide begins by showing the .env file containg the environmental variables
- mySQL is then leveraged to drop the 'ecommerce_db' if it exist and create a new empty 'ecommerce_db' database.
- The database is then seeded using the npm run seed functionallity to execute the index file within the seeds folder
- The app is then initialized by using npm start to execute the server.js file.

- API Endpoint Testing:
    - Once the server is listening on the local host a get all and get by ID request is shown for the categories, products and tags.
        - The get route for the categories shows the associated products linked through the products category_id
        - The get route for the tags shows the associated products linked through the tag_id
        - The get route for the products shows the associated tags linked through the product_id
    - The post and get routes are then shown for a new Category.
        - The new items are created with an automatically generated id.
        - The items are then shown with a get request by the newly generated id.
        - A put request is then sent to update the newly created category and the category is displayed by id to confirm it has been updated.
        - The same steps are then taken to display the paths for the products and tags. 
    - The delete paths are then shown for a category, product and tag.
        - After an item has been deleted the get by id route is used to confirm that the item no longer exists within the database.

## License
N/A