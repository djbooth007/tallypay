# Tallycoin Bitcoin Fundraising

Tallycoin (at https://tallyco.in/) is a non-custodial Bitcoin fundraising platform.

One component of the website is the payment plugin named Tallypay.

## Tallypay

![Image of Tallypay](https://github.com/djbooth007/tallycoin/blob/master/img/tallypay.png)

Tallypay is an independent website plug-in that hooks in to the Tallycoin API. You will need an account via https://tallyco.in/ to enter your Bitcoin and Lightning Network payment information.

You can add Tallypay to your website to receive donations.

1. Add the following to the &lt;head&gt; tag of your website (only once).
  
`<script src="tallypay.js" type="text/javascript"></script>`
 
2. Add the following to the main body of your website.

`<div class="tallypay" data-user="yourUsername"></div>`

### Advanced Options

The plug-in looks at the data-* attributes to determine what to do.

Eg #1, data-user="yourUsername" will retrieve information about your account.

Eg #2, data-fundid="" is optional and specifies any of your fundraisers set by data-fundid="fundraiser_id".

`<div class="tallypay" data-user="yourUsername" data-fundid="fundraiser_id" ></div>`

### Callback

When a payment has been made, it is possible for the plug-in to call an external function specified in the data-onpayment attribute.

An array will be returned to your function eg, ['satoshi_amount' => 1000, 'payment_method' => 'lightning']

`<div class="tallypay" data-user="yourUsername" data-onpayment="payment_success_function"></div>`

### Theme

Don't like the default light theme? You can add the data-theme="dark" attribute.

`<div class="tallypay" data-user="yourUsername" data-theme="dark"></div>`

### Make It a Button

By default, the plug-in will appear as a panel (same as the preview image above). To use a small button instead, add the data-size="button" attribute.

When using a button, the button text must also be specified with the data-button_text="some text" attribute.

`<div class="tallypay" data-user="yourUsername" data-size="button" data-button_text="Buy Me a Coffee" ></div>`

### Make It an Image

If you want to use your own image, add the data-image="{your image location}" attribute.

`<div class="tallypay" data-user="yourUsername" data-image="https://yourdomain.com/imgsource.jpg" ></div>`

### Licence

This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License, version 3, as published by the Free Software Foundation.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.

View a copy of the GNU General Public License at http://www.gnu.org/licenses/.
