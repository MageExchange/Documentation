---
layout: default
title: GDPR v1.1.0
description: This documentation contains everything you need to about the Magento 2 GDPR module from installing & managing this extension.
permalink: /gdpr/v1.1.0/
---

## GDPR Manual - Magento 2 Extension - v1.1.0
Welcome to the **GDPR** Magento module documentation! As always, we appreciate your business!

This documentation contains everything you need to know from installing the module to managing the module.

Our [GDPR Magento 2 module](https://www.mageexchange.com/gdpr-magento-2) Our Magento 2 GDPR module helps your business to comply with the latest legislative EU requirements. This helps to protect your customer's data by allowing your customer's to have control over the data they want to share or remove.


### Getting Started
Simply visit your account dashboard and click on the link labeled **My Downloadable Products** to locate your purchased module. Finally, download your purchased module in order to get started.


### Installation Manual
At this point, we assume you have already downloaded your purchased module. If you have not, please visit the Getting Started section of this document before proceeding. If you did not purchase the "Module Installation" option during checkout and would like us to install this module for you, simply purchase this option here: [Installation Service](https://www.mageexchange.com/module-installation-service-magento-2)


### Installing & Activating the Module
1. It is best practice to make a backup of your database and Magento installation directory before installing any Magento module so you are able to safely roll back should any problems arise during the install.
2. Create a file called .maintenance.flag (using your favorite FTP/SFTP software; e.g. Filezilla, Transmit, ...) and place it inside your Magento store root directory inside of the var folder. This will put your Magento store into maintenance mode. Please note: Be sure to use login to your server as the appropriate Magento file owner for the directory before proceeding to ensure proper file permissions.
3. Unzip the downloaded module.
4. Move the appropriate Magento module files located inside this folder to your existing Magento store root directory without overwriting any existing core Magento files.
5. Login to your server using a command line interface (CLI) tool and navigate to your Magento's store root directory. Example: ```cd /path/to/your/Magento/store/public_html```
6. Run the following command: ```php -f bin/magento module:enable MageExchange_Base MageExchange_Gdpr --clear-static-content```
7. Run the following command:
```php -f bin/magento setup:upgrade```
8. Run the following command: ```rm -rf var/view_preprocessed/* pub/static/* generated/*```
9. Run the following command: ```php -f bin/magento cache:clean```
10. If your store is currently in production mode, please run the following command: ```php bin/magento setup:di:compile```
11. Run the following command: ```php -f bin/magento setup:static-content:deploy```
12. Remove the .maintenance.flag file that you created to take the store out of maintenance mode.


### User Configuration
### General Settings
**Enable GDPR:** This will enable the GDPR module

### Customer Permissions
**Delete Customer Address:** Allow the customer to delete their billing and shipping addresses.

**Delete Cookies:** Allow the customer to delete store cookies. This version currently deletes the amz_auth_err, amz_auth_logout, guest-view, login_redirect, mage-cache-sessid, mage-cache-storage, mage-cache-storage-section-invalidation, persistent_shopping_cart, private_content_version, product_data_storage, recently_compared_product, recently_compared_product_previous, recently_viewed_product, recently_viewed_product_previous, section_data_ids, stf, store, __utma, __utmt, __utmb, _utmz and __utmv cookies.

**Delete Account:** Allow the customer to delete their account. This will automatically delete user cookies, abandoned cart data, addresses and anonymize all their orders depending on your GDPR settings. e.g. If everything is enabled, all cookies and data will be erased and/or anonymized at once.

### Customer Order Anonymization
**Allow Anonymized Orders:** This will allow the customer to anonymize the order information on their orders including the invoice, shipment and credit memo. The customer's first name, last name, email address, billing address, shipping address and phone number will be anonymized forever.

**Anonymize Orders Not Closed/Completed:** **Note**: "Allow Anonymized Orders" must also be enabled for this option to work. If enabled, this will allow the customer to anonymize orders in any state. If disabled, the customer can only anonymize orders that have been marked with a status of complete, closed or cancelled. If disabled you must anonymize the remaining associated customer order data that is not marked as complete, closed or cancelled at the customer's request.

**Anonymized First Name:** Enter the first name that you would like to use to replace the actual customer's first name. If left blank, Xxxxxxxxxxx will be used to replace their first name.

**Anonymized Last Name:** Enter the last name that you would like to use to replace the actual customer's last name. If left blank, Xxxxxxx will be used to replace their last name.

**Anonymized Email:** Enter the email address that you would like to use to replace the actual customer's email address. If left blank, anonymized@fakeemail.com will be used to replace their email address.

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
