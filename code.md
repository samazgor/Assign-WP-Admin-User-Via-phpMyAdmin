### SQL queries for adding admin user in the WordPress.


```sql
INSERT INTO `your_db_name`.`wp_users` (`ID`, `user_login`, `user_pass`, `user_nicename`, `user_email`, `user_url`,`user_registered`, `user_activation_key`, `user_status`, `display_name`) VALUES ('4', 'new_admin_username', MD5('your_password'), 'Your Name', 'newadmin@domain.com', 'http://www.domain.com/', '2011-06-07 00:00:00', '', '0', 'Your Name');

INSERT INTO `your_db_name`.`wp_usermeta` (`umeta_id`, `user_id`, `meta_key`, `meta_value`) VALUES (NULL, '4', 'wp_capabilities', 'a:1:{s:13:"administrator";s:1:"1";}');

INSERT INTO `your_db_name`.`wp_usermeta` (`umeta_id`, `user_id`, `meta_key`, `meta_value`) VALUES (NULL, '4', 'wp_user_level', '10');
```

Replace the following values with your own databse values

1. `your_db_name`
2. `new_admin_username`
3. `your_password`
4. `Your Name`
5. `newadmin@domain.com`
6. `http://www.domain.com/`
7. `Your Name`
