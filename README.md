# reset_wp_pass_mysql_command

 "mysql -u root -p" (Logs in to MySQL/MariaDB)

 Enter your password at the prompt.

 "use name-of-database" (Selects your WordPress database)

 "show tables LIKE '%users';" (Finds the WordPress user table)

 "SELECT ID, user_login, user_pass FROM name-of-table-you-found WHERE user_login = 'username';" (Observe the encrypted password)

 "UPDATE name-of-table-you-found SET user_pass=MD5('new-unencrypted-password') WHERE user_login = 'username';"  (Updates the database with the encrypted password)

 "SELECT ID, user_login, user_pass FROM name-of-table-you-found WHERE user_login = 'username';" (Confirm that it was changed)

 "exit" (Exits the MySQL client)

 Login to WordPress using the username and password that you've altered.
 
 
 Followed https://codex.wordpress.org/Talk:Resetting_Your_Password 
