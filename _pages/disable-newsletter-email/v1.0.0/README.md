---
layout: default
title: Magento 2 Disable Newsletter Email Module v1.0.0
description: This documentation contains everything you need to about the Magento 2 Disable Newsletter Confirmation Email module from installing the module to managing the module.
permalink: /disable-newsletter-email/v1.0.0/
---

## Disable Newsletter Sign Up Emails Manual - Magento 2 Extension - v1.0.0
Welcome to the **Disable Newsletter Sign Up Emails** Magento module documentation! As always, we appreciate your business!

This documentation contains everything you need to know from installing the module to managing the module.

Our [Disable Newsletter Confirmation Email Magento 2 module](https://www.mageexchange.com/disable-newsletter-sign-up-emails-magento-2) allows you to disable the newsletter sign up confirmation emails. This is especially helpful when you are receiving a lot of spam or bot newsletter sign ups and want to lower your email bounce rate.


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
6. Run the following command: ```php -f bin/magento module:enable MageExchange_NewsletterSignupNotification --clear-static-content```
7. Run the following command:
```php -f bin/magento setup:upgrade```
8. Run the following command: ```php -f bin/magento cache:clean```
9. Run the following command: ```rm -rf var/view_preprocessed/* pub/static/* generated/*```
10. Run the following command: ```php -f bin/magento setup:static-content:deploy```
11. If your store is currently in production mode, please run the following command: ```php bin/magento setup:di:compile```
12. Remove the .maintenance.flag file that you created to take the store out of maintenance mode.


### User Configuration
**Disable Confirmation Sign Up Email:** This will enable or disable this functionality. When enabled, new newsletter subscribers will no longer be sent a confirmation email.

**Need to Confirm:** Change this method to No.


### Troubleshooting
We will update this section with common technical questions or issues. However, at this time there are none.

Should you need any support or have valuable feedback, please feel free to open a ticket at anytime at [https://www.mageexchange.com/contact](https://www.mageexchange.com/contact).


### Thank You
We would just like to take this time to say thank you for purchasing from MageExchange! Your business is greatly appreciated and we hope you come back to us for all of your Magento 2 module needs in the future!
