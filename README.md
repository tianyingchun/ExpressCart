# ExpressCart

**Alpha release - Please report any bugs**

ExpressCart is a Shopping Cart built with [Nodejs](https://nodejs.org/) and [ExpressJS](http://expressjs.com/). The application uses an embedded database ([nedb](https://github.com/louischatriot/nedb)) for easy installation.
The application is designed to be easy to use and install and based around search rather than nested categories. Simply search for what you want and select from the results.

ExpressCart uses powerful Lunr.js to index the products to enable the best search results possible.

Demo: [http://cart.mrvautin.com](http://cart.mrvautin.com)

### Installation

1. Clone Repository: `git clone https://github.com/mrvautin/ExpressCart.git && cd ExpressCart`
2. Install dependencies: `npm install`
3. Start application: `npm start`
4. Go to  [http://127.0.0.1:7777](http://127.0.0.1:7777) in your browser

### Features

- **Seach**: ExpressCart is a search based Shopping Cart backed by [Lunr.js](https://github.com/olivernn/lunr.js/) indexing to create the best possible results on searches. 
- **Backend**: ExpressCart uses the pure javascript [nedb](https://github.com/louischatriot/nedb) embedded database. This means no external databases need to be setup.
- **Design**: ExpressCart is meant to be simple flat design. 
- **Responsive**: ExpressCart is built using Bootstrap allowing it to be responsive and work on all devices. The `admin` can be a little difficult editing Markdown on smaller screens.

### Screenshots

![Homepage](https://raw.githubusercontent.com/mrvautin/mrvautin.github.io/master/images/ExpressCart/Index-rootview.png)
![Product View](https://raw.githubusercontent.com/mrvautin/mrvautin.github.io/master/images/ExpressCart/Index-product.png)
![Cart view](https://raw.githubusercontent.com/mrvautin/mrvautin.github.io/master/images/ExpressCart/Index-cart.png)
![Checkout view](https://raw.githubusercontent.com/mrvautin/mrvautin.github.io/master/images/ExpressCart/Index-checkout.png)
![Admin New product](https://raw.githubusercontent.com/mrvautin/mrvautin.github.io/master/images/ExpressCart/Admin-addproduct.png)
![Admin Edit product](https://raw.githubusercontent.com/mrvautin/mrvautin.github.io/master/images/ExpressCart/Admin-editproduct.png)
![Admin Order list](https://raw.githubusercontent.com/mrvautin/mrvautin.github.io/master/images/ExpressCart/Admin-orderlist.png)
![Admin products](https://raw.githubusercontent.com/mrvautin/mrvautin.github.io/master/images/ExpressCart/Admin-products.png)
![Admin View order](https://raw.githubusercontent.com/mrvautin/mrvautin.github.io/master/images/ExpressCart/Admin-vieworder.png)

### Admin

Visit: [http://127.0.0.1:7777/admin](http://127.0.0.1:7777/admin) 

A new user form will be shown where a user can be created.

### Config

There are are a few configurations that can be made which are held in `/config/default.json`. If any values have been changed the app will need to be restarted.

Example config file
```
{
    "application": {
        "cart_title": "ExpressCart",
        "number_products_index": 8,
        "base_url": "http://localhost:7777",
        "flat_shipping": 10.00,
        "free_shipping_amount": 100.00,
        "paypal_username": "sandboxusername.gmail.com",
        "paypal_password": "4913720873",
        "paypal_signature": "RF0gpHVXEWAFcWxV7LmcPrNwnk7R3bYYYRCpSSR21C7fd0vWMlDl31Ah",
        "paypal_cart_description": "ExpressCart Payment",
        "paypal_currency": "USD"
    }
}
```

### TODO

- Email receipts
- More flexible shipping options/estimate etc
- SEO improvements
- Social sharing
- UI improvements

### Running in production

Using [PM2](https://github.com/Unitech/pm2) is the easiest and best option for running production websites.
See the [PM2](https://github.com/Unitech/pm2) for more information or a short guide here: [https://mrvautin.com/running-nodejs-applications-in-production-forever-vs-supervisord-vs-pm2/](https://mrvautin.com/running-nodejs-applications-in-production-forever-vs-supervisord-vs-pm2/).