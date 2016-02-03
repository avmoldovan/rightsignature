RightSignature API OAuth integration PHP
===============================================
This is an example application to demonstrate how to use some of RightSignature's API calls using OAuth. 

WARNING: Please note that we are not PHP developers and this source code should only be used as a reference.
We are open to Pull Requests if you have improvements to the code.

SETUP
-----
1. Create the database (assuming root is your root user):
	mysqladmin create -uroot rs_php

2. Create Tables:
	mysql -uroot rs_php < settings.sql
	mysql -uroot rs_php < documents.sql
	mysql -uroot rs_php < templates.sql
	mysql -uroot rs_php < users.sql

3. Get your API tokens from RightSignature.com, set the Callback URL to be to'/setup/callback.php' ex. "http://localhost:8888/setup/oauth_callback.php"

4. Copy 'config/creds.php.example' to 'config/creds.php' and update credentials in config/creds.php

5. Get generate Request Token, visit authentication url, save OAuth Access Token and Verifier to settings table. There is a page that will do this for you:
		/setup/save_rs_access.php

6. Run your favorite webserver and host the files minus the 'setup' directory

How to Contribute
-----------------
1. Fork repo: http://help.github.com/fork-a-repo/
2. Commit and push your changes in your forked repo.
3. Submit a Pull Request: http://help.github.com/pull-requests/

Contributors:
 * Cary Dunn
 * Alex Chee

Copyright
---------
Released under an MIT License. See LICENSE for details.
