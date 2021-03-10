# Pimcore Demo

This is a demo of Pimcore built with vagrant and ansible.

## Prerequisites:

* virtualbox
* vagrant
* ansible

Ansible extras:

* `ansible-galaxy collection install community.mysql`

## Installation Notes

It is currently set to listen on `localhost:8085`

Stack:
* Nginx
* PHP-FPM
* MySQL

I added most of the additional tools described here [Additional Tools Installation](https://pimcore.com/docs/pimcore/current/Development_Documentation/Installation_and_Upgrade/System_Setup_and_Hosting/Additional_Tools_Installation.html)

What is still missing from the Additional Tools:

* Wkhtmltopdf
* SQIP


Database Creds
* Pimcore Database User: pimcore
* Pimcore Database Password: pimcore
* Pimcore Database Name: pimcore

App Creds
* Admin username: admin
* Admin password: admin
* `http://localhost:8085/admin/login`

File location: `/var/www/pimcore`

The Nginx config is mostly as suggested here [Nginx Configuration](https://pimcore.com/docs/pimcore/current/Development_Documentation/Installation_and_Upgrade/System_Setup_and_Hosting/Nginx_Configuration.html) with the following exceptions:

* No SSL is configured
* I had to remove the CSP security header so that remote files would load
