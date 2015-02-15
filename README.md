CodeIgniter-Sample-Project-By-Dinesh

Sample administrator panel using CodeIgniter 2.1.2 with Mysql and Twitter Bootstrap.

READ IT FIRST!!!: Guys, i've made this project with the idea to help the community, the idea was to receive suggestions and grow the project along with the community.

Unfortunately (or not) one week after i did this project, i started to work with Ruby and Rails, and kind of did left the php and this project as well. It's too sad check the project one year after its creation and see lots of issues without a single pull request...

Issues are a great opportunity to join and contribute to open source as well help the project to grow. There are some issues with the fix in the comment but no pull requests..

So please... make yourself comfortable to help!

https://github.com/DineshShriVIshwakarma/CodeIgniter-admin-panel/edit/master/README.md

Requirements

    Bootstrap 2.0.4+
    jQuery 1.7.1+

Functionalities:

    Signup/Login/Logout
    Create, insert, edit and delete products
    Create, insert, edit and delete manufacturers
    All forms with back end validation
    List data content with pagination, search, and filters

Screenshots

Instructions

    Setup your database in application/config/database.php
    Dump the mysql at the bottom of this readme
    Change $config['base_url'] in application/config/config.php
    Access your project url
    Signup and enjoy!

Mysql Dump

CREATE TABLE `ci_cookies` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `cookie_id` varchar(255) DEFAULT NULL,
  `netid` varchar(255) DEFAULT NULL,
  `ip_address` varchar(255) DEFAULT NULL,
  `user_agent` varchar(255) DEFAULT NULL,
  `orig_page_requested` varchar(120) DEFAULT NULL,
  `php_session_id` varchar(40) DEFAULT NULL,
  `created_at` datetime DEFAULT NULL,
  `updated_at` datetime DEFAULT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

CREATE TABLE `ci_sessions` (
  `session_id` varchar(40) NOT NULL DEFAULT '0',
  `ip_address` varchar(45) NOT NULL DEFAULT '0',
  `user_agent` varchar(120) NOT NULL,
  `last_activity` int(10) unsigned NOT NULL DEFAULT '0',
  `user_data` text NOT NULL,
  PRIMARY KEY (`session_id`),
  KEY `last_activity_idx` (`last_activity`)
) ENGINE=MyISAM DEFAULT CHARSET=latin1;

CREATE TABLE `manufacturers` (
  `id` int(11) unsigned NOT NULL AUTO_INCREMENT,
  `name` varchar(50) DEFAULT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

CREATE TABLE `membership` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `first_name` varchar(255) DEFAULT NULL,
  `last_name` varchar(255) DEFAULT NULL,
  `email_addres` varchar(255) DEFAULT NULL,
  `user_name` varchar(255) DEFAULT NULL,
  `pass_word` varchar(32) DEFAULT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

CREATE TABLE `products` (
  `id` int(11) unsigned NOT NULL AUTO_INCREMENT,
  `description` varchar(40) DEFAULT NULL,
  `stock` double DEFAULT NULL,
  `cost_price` double DEFAULT NULL,
  `sell_price` double DEFAULT NULL,
  `manufacture_id` int(11) DEFAULT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=latin1;



