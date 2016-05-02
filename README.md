# ExpressCart

**Alpha release - Please report any bugs**

ExpressCart is a Shopping Cart built with [Nodejs](https://nodejs.org/) and [ExpressJS](http://expressjs.com/). The application uses an embedded database ([nedb](https://github.com/louischatriot/nedb)) for easy installation.
The application is designed to be easy to use and install and based around search rather than nested categories. Simply search for what you want and select from the results. ExpressCart uses powerful Lunr.js to index the products to enable the best search results possible.

Demo: [http://expresscart.mrvautin.com](http://expresscart.mrvautin.com)

### Installation

### Git

1. Clone Repository: `git clone https://github.com/mrvautin/ExpressCart.git && cd ExpressCart`
2. Install dependencies: `npm install`
3. Start application: `npm start`
4. Go to  [http://127.0.0.1:7777](http://127.0.0.1:7777) in your browser

### NPM
1. Install from NPM: `npm install expresscart`
2. Move folder from `node_modules`: `mv node_modules/expresscart/ ./ExpressCart`
3. Enter folder: `cd ExpressCart`
4. Install dependencies: `npm install`
5. Start application: `npm start`
6. Visit [http://127.0.0.1:7777](http://127.0.0.1:7777) in your browser

### Features

- **PayPal**: ExpressCart has built in PayPal Express Checkout.
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

Paypal details can be obtained by logging into your PayPal account.

- `cart_title` refers to the title shown on  the top of your cart navigation menu. If you would like a logo in it's place you will have to edit the `/views/layouts/layout.hbs`.
- `number_products_index` refers to the amount of products shown on the homepage of your cart.
- `base_url` refers to the URL of your cart. **Note: Ensure there is no trailing slash**
- `flat_shipping` refers to the flat shipping rate if the total card amount is less than the value set in `free_shipping_amount`.
- `free_shipping_amount` refers to the minimum spend for a customer to receive free shipping. If free shipping is never offered, set this value to something really high. Eg: 9999999.00
- `paypal_username` refers to the value obtained from your PayPal account login
- `paypal_password` refers to the value obtained from your PayPal account login
- `paypal_signature` refers to the value obtained from your PayPal account login
- `paypal_cart_description` refers to the value shown to the user when redirected to the PayPal payment page
- `paypal_currency` refers to a valid currency to accept payments. PayPal does the conversion

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

### Styling/design

By default `ExpressCart` uses the [flatly](https://bootswatch.com/flatly/) `Bootswatch` theme. This can be quickly changed by commenting/uncommenting other themes in `/views/layouts/layout.hbs` to the desired theme. 

### Contribute
Looking for help to develop the software further. There isn't any good Nodejs shopping cart software and ExpressCart could fill the void. Please submit any issues and pull requests to make this better. **Looking for anyone with security experience to cast an eye over and pickup and issues.**

### TODO

- Email receipts
- More flexible shipping options/estimate etc
- SEO improvements
- Social sharing
- UI improvements

### Running in production

Using [PM2](https://github.com/Unitech/pm2) is the easiest and best option for running production websites.
See the [PM2](https://github.com/Unitech/pm2) for more information or a short guide here: [https://mrvautin.com/running-nodejs-applications-in-production-forever-vs-supervisord-vs-pm2/](https://mrvautin.com/running-nodejs-applications-in-production-forever-vs-supervisord-vs-pm2/).

## License

[The MIT License](https://github.com/mrvautin/Express/tree/master/LICENSE)