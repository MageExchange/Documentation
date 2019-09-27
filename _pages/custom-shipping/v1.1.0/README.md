---
layout: current
title: Custom Shipping v1.1.0
description: This documentation contains everything you need to about the Magento 2 Custom Shipping module from installing & managing this extension.
canonical_url: https://documentation.mageexchange.com/custom-shipping/v1.1.0/
permalink: /custom-shipping/v1.1.0/
---

## Custom Shipping Manual - Magento 2 Extension - v1.1.0
Welcome to the **Custom Shipping** Magento module documentation! As always, we appreciate your business!

This documentation contains everything you need to know from installing the module to managing the module.

Our [Custom Shipping Magento 2 module](https://www.mageexchange.com/custom-shipping-method-magento-2) is light weight and flexible. It allows your company to easily add a custom shipping method to all your Magento storefronts.


### Getting Started
Simply visit your account dashboard and click on the link labeled **My Downloadable Products** to locate your purchased module. Finally, download your purchased module in order to get started.


### Installation Manual
At this point, we assume you have already downloaded your purchased module. If you have not, please visit the Getting Started section of this document before proceeding. If you did not purchase the "Module Installation" option during checkout and would like us to install this module for you, simply purchase this option here: [Installation Service](https://www.mageexchange.com/module-installation-service-magento-2)


### Installing & Activating the Module
1. It is best practice to make a backup of your database and Magento installation directory before installing any Magento module so you are able to safely roll back should any problems arise during the install.
2. Create a file called .maintenance.flag (using your favorite FTP/SFTP software; e.g. Filezilla, Transmit, ...) and place it inside the var/ directory located in your Magento store root directory. This will put your Magento store into maintenance mode. Please note: Be sure to use login to your server as the appropriate Magento file owner for the directory before proceeding to ensure proper file permissions.
3. Unzip the downloaded module.
4. Move the appropriate Magento module files located inside this folder to your existing Magento store root directory without overwriting any existing core Magento files.
5. Login to your server using a command line interface (CLI) tool and navigate to your Magento's store root directory. Example: ```cd /path/to/your/Magento/store/public_html```
6. Run the following command: ```php -f bin/magento module:enable MageExchange_Base MageExchange_CustomShipping --clear-static-content```
7. Run the following command:
```php -f bin/magento setup:upgrade```
8. Run the following command: ```rm -rf var/view_preprocessed/* pub/static/* generated/*```
9. Run the following command: ```php -f bin/magento cache:clean```
10. If your store is currently in production mode, please run the following command: ```php bin/magento setup:di:compile```
11. Run the following command: ```php -f bin/magento setup:static-content:deploy```
12. Remove the .maintenance.flag file that you created to take the store out of maintenance mode.


### User Configuration
**Enabled:** This will enable or disable the Custom Shipping module

**Title:** This will set the title of the custom shipping method. e.g. Flat Rate

**Method Name:** This is the method name of the custom shipping. e.g. White Glove Delivery

**Shipping Cost:** This is the flat rate shipping cost per order for this new method.

**Ship to Applicable Countries:** Allow all Countries our specific Countries

**Ship to Specific Countries:** Choose specific Countries that you would like to use this shipping method for if "Specific Countries" was selected in the previous setting.

**Show Method if Not Applicable:** Decide whether or not to show this method if it isn't available.

**Displayed Error Message:** If "Show Method if Not Applicable" was set to yes, display a custom method to the user if the method isn't available for them.

**Sort Order:** Set the order this shipping method show be displayed in.


### Troubleshooting
We will update this section with common technical questions or issues. However, at this time there are none.

Should you need any support or have valuable feedback, please feel free to open a ticket at anytime at [https://www.mageexchange.com/contact](https://www.mageexchange.com/contact/).   
   
   
### Change Log
(**1.1.0**) 2019-09-22   
   
**Improvements**   
- Added our base module which allows you to easily check if there are updates to any of your MageExchange modules without ever leaving your backend.   
- General code cleanup.   
   
   
### Thank You
We would just like to take this time to say thank you for purchasing from MageExchange! Your business is greatly appreciated and we hope you come back to us for all of your Magento 2 module needs in the future!
