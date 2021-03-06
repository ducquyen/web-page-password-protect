# Web Page Password Protect

**Source**: http://www.zubrag.com/scripts/password-protect.php

Password protect your content with Web Page Password Protect by just adding one line of PHP code to your page source. Script will present user with password entry form, and will not let visitor see your private content without providing a password.

Multiple user accounts support, improved security, automatic logout, and manual logout feature.

**Usage**:
- Save `password_protect.php` somewhere on your server  
- Update it with your desired password or login/password pair. Use any plain text editor to accomplish this step. Sample editors: Notepad (Windows) or vi (Unix).  
- Open script in your browser with "help" parameter to see the line of code to add to every page you would like to be password protected.
Example: `password_protect.php?help`
It will show you protection code to include into your pages. Sample protection code would look like this (yours will be different):  
`<?php include("/home/users/htdocs/security/password_protect.php"); ?>`  
- Add that line of code to each php page you would like to protect at the very beginning of the page source (it must be the first line).
For example you want to protect page protect-me.php. Open it for editing, and add the protection string (see above on how to get the protection string) at the beginning. So resulting code would look like:  
`<?php include("/home/users/htdocs/security/password_protect.php"); ?>`  
... here, at the second line starts your page code ...
- Setup **Logout URL** in the script  
If you look at the `password_protect.php` source code you'll see following:  
`// User will be redirected to this page after logout`  
`define('LOGOUT_URL', 'http://www.example.com/');`
- Add **Logout** link on your website  
Add following HTML code on your site pages wherever you want a logout link to be shown:  
`<a href="http://www.example.com/path/to/protected/page.php?logout=1">Logout</a>`  
Upon logout script will redirect user to the URL you specified on `LOGOUT_URL`.
- Suggested file permissions `440` ( `-r--r-----` ).
