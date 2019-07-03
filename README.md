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
* Official version: 2.3.4++ (catalog design is not supported)
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

In admin/includes/application_top.php and
includes/application_top.php

At the end of the file add

```php
  require 'includes/functions/blog.php'; //  blog pro add-on
```

4. Open Administration Tool (Backend) in menu "Blog" click on the link "Start".

5. Install module:

- in menu Modules -> Boxes -> button "Install Module" -> select modules (Blog Archives, Blog Search, Popular Posts, Recent Comments, Recent Posts, Rubrics) -> button "Install Module"
- in menu Modules -> Content -> button "Install Module" -> select modules (Post Subscriptions List, Comments To Post, Next/Previous Post Links, Post Social Bookmarks, Related Products) -> button "Install Module"
- in menu Modules -> Header Tags -> button "Install Module" -> select modules (Blog Feed, Blog Rich Snippets, Post Open Graph Meta Tags, Post Meta Description, Post Title, Rubric Meta Description, Rubric Title, Rubrics Rel Next/Previous, Twitter Post Card) -> button "Install Module"
