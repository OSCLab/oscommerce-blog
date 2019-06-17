# Blog Pro - osCommerce add-on
This module will integrate a professional blogging system on your osCommerce store without a need to install a separate CMS on your sub-domain. Make blogging an effective part of your marketing strategy with Blog Pro.

Why your store needs a personal blog?

* Generate new leads and drive targeted traffic to a web store
* Increase search engines ranking
* Quality content for social media by linking to a blog
* Stand out among the competitors
* Gather clients feedback in comments and improve your service

Compatible With:

* Community Edition version: All 
* Official version: 2.3++ (catalog design is not supported)
* Minimum PHP Version: 7.0

## Installation

1. Backup all files and database!

2. Unzip the archive and upload the files on server.

Files that will be replaced on the server:

- includes/modules/social_bookmarks/sb_digg.php
- includes/modules/social_bookmarks/sb_email.php
- includes/modules/social_bookmarks/sb_facebook.php
- includes/modules/social_bookmarks/sb_facebook_like.php
- includes/modules/social_bookmarks/sb_google_plus_one.php
- includes/modules/social_bookmarks/sb_google_plus_share.php
- includes/modules/social_bookmarks/sb_pinterest.php
- includes/modules/social_bookmarks/sb_twitter.php
- includes/modules/social_bookmarks/sb_twitter_button.php 

3. Manually make changes.

In admin/languages.php
 
after

```php
         tep_db_query("insert into " . TABLE_LANGUAGES . " (name, code, image, directory, sort_order) values ('" . tep_db_input($name) . "', '" . tep_db_input($code) . "', '" . tep_db_input($image) . "', '" . tep_db_input($directory) . "', '" . tep_db_input($sort_order) . "')");

         $insert_id = tep_db_insert_id();
```
 
 add 
 
```php
       // start blog pro add-on
       tep_insert_rubrics_description($insert_id);
       tep_insert_posts_content($insert_id);
       // end blog pro add-on
```
 
 after
 
```php
          tep_db_query("delete from " . TABLE_ORDERS_STATUS . " where language_id = '" . (int)$lID . "'");
 
          tep_db_query("delete from " . TABLE_LANGUAGES . " where languages_id = '" . (int)$lID . "'");
```
 add 
 
```php
        // start blog pro add-on
        tep_db_query("delete from rubrics_description where language_id = '" . (int)$lID . "'");
        tep_db_query("delete from posts_content where language_id = '" . (int)$lID . "'");
        // end blog pro add-on
```
In admin/includes/application_top.php and
includes/application_top.php

At the end of the file add

```php
  require 'includes/functions/blog.php'; //  blog pro add-on
```

4. Open Administration Tool (Backend) in menu Blog click Start
