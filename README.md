### Change rewritemode to allow pretty URL

#### Step I: Activate mod_rewrite

Run below command to enable this module.
`sudo a2enmod rewrite`

#### Step II: Set AllowOverride directive to all in your vhost file

If you are using virtual hosts open /etc/apache2/sites-available/{somename}.conf otherwise /etc/apache2/apache2.conf and change :
`Options Indexes FollowSymLinks
      AllowOverride all
      Require all granted`

#### Step III: Restart apache

Restart apache server for the changes to take effect.
`sudo service apache2 restart`
That’s it. Your .htaccess file rules should now work.
