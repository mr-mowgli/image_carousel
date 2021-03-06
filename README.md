# Carousel
Image Carousel

# Welcome to the image carousel.

In order to get setup run the following scripts:

1) Install Dependencies: npm install

2) Seeding Script:
  - open mongo instance in terminal: mongo
  - choose database: use carousel
  - clear collection: db.images.remove({})
  - in a seperate terminal: npm run dbSetup

3) Server Start Script: npm start

4) Webpack Script: npm run build

5) Carousel should be rendered to DOM


Testing Script: npm test

Have Fun!

# CRUD Operations

## Create:

  request body must include an image object

    method: get

    endpoint: /image

    ------------------------------------

    product:   product number (required)

    imageName: title of the image

    color:     product color variation

    url:       url of the actual image (required)

    alt:       alternate

## Retrieve:
    method: post

    endpoint: /products/:product/

    params: :product is the product number defining each primary record

    returns: array of all images associated with the product in JSON format

    ------------------------------------

    product:   product number

    imageName: title of the image

    color:     product color variation

    url:       url of the actual image



    alt:       alternate

## Update:

  request body must have an image object with at least product and url keys. The item matching those two keys will be updated with the values at the remaining keys

    method: put

    endpoint: /image

    ------------------------------------

    product:   product number (required)

    imageName: title of the image

    color:     product color variation

    url:       url of the actual image (required)

    alt:       alternate

## Delete:

### Delete single image:

  request body must have an image object with at least product and url keys. The item matching those two keys will be deleted
  method: delete

    endpoint: /image

    ------------------------------------

    product: product number (required)

    url:     url of the actual image (required)

### Delete all images related to a product:

  request body must have an image object with at least product and url keys. The item matching those two keys will be deleted

    method: delete

    endpoint: /product

    ------------------------------------

    product: product number (required)

