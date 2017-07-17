# Facebook messenger extension
Integration with Facebook messenger API. You will be able to chat with Facebook page users directly in lhc back office.
 * Supports multiple pages at once.
 * Each page chat can be assigned to custom department.

# Example of callback url
https://example.com/fbmessenger/callback/<id>


# Installation in your LHC server
 * Upload the files to your /extension folder
 * Install database either by executing doc/install.sql file or executing this command php "cron.php -s site_admin -e fbmessenger -c cron/update_structure"
 * Create facebook page in Modules -> Facebook chat -> Facebook pages -> Register new page
  if you dont see this in Module, check your settings.ini.php
 * Once page is created you will see what callback url you have to put in facebook webhook. URL is presented in list.
 
# Installation inside Facebook as Developer 
 * You have to configure facebook app according to this tutorial https://developers.facebook.com/docs/messenger-platform/guides/quick-start/
 * Your facebook application has to have "pages_messaging" permission for lhc to be able to extract visitor information and be able to send messages back to lhc. For that you will have to submit application and wait for FB to review it.
 * Before facebook validates your application keep settings "verified" false (in facebook page configuration). After facebook has reviewed your application set "verified" to true. So you will be able to send a messages. During testing, if you add some developer, you can set it to true to see how it works.
 
# How it works
Once visitor writes a message in facebook page. You will receive a chat with visitor.

# Todo
 * Add support for images, not just plain messages.
 * Add support for automated hosting environment.
