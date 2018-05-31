# Appendix 1. Create a Protected OJS 3 Sandbox Staged with Git

The following document describes a general workplan for creating a git-based sandbox of a production journal that is not currently on git. It provides instructions on how to limit accidental access, outgoing email, etc. YMMV. Adapt for your own environment; use at your own risk.

## Prepare the Git environment

The README here: [https://github.com/pkp/ojs](https://github.com/pkp/ojs) has instructions on installing from git. What we do is as follows:

1. Create MySQL OJS user and database. The command we use is as follows; it may be different for you depending on your environment, access to root, etc.:  
   * mysql -u root -e "CREATE DATABASE \\`ojs-sandbox\\` DEFAULT CHARACTER SET UTF8; GRANT ALL ON \\`ojs-sandbox\\`.\* TO \\`ojs\\`@localhost IDENTIFIED BY 'ojs'" -p
2. Checkout stable branch from github:
   * cd &lt;httpd-docs-folder&gt; \(path will be specific to your Apache install\)
   * git clone -n [https://github.com/pkp/ojs.git](https://github.com/pkp/ojs.git) ./
   * git checkout -b ojs-3\_1\_0 --no-track origin/ojs-stable-3\_1\_0 \(you will want to update this reference to pjs-stable-3\_1\_1 once that branch is available on Tuesday-ish\)
   * cp config.TEMPLATE.inc.php config.inc.php
   * chmod -R 755 \*
   * chmod 600 config.inc.php
3. Fetch corresponding PKP library and checkout stable branch from github:
   * git submodule update --init --recursive
   * cd lib/pkp
   * git checkout -b ojs-3\_1\_0 --no-track origin/ojs-stable-3\_1\_0 \(make sure this branch corresponds to the same branch referenced in b\) above\)
4. Install composer:
   * cd ../..
   * php -r "copy\('[https://getcomposer.org/installer', 'composer-setup.php](https://getcomposer.org/installer',%20'composer-setup.php)'\);"
   * php -r "if \(hash\_file\('SHA384', 'composer-setup.php'\) === '544e09ee996cdf60ece3804abc52599c22b1f40f4323403c44d44fdfdd586475ca9813a858088ffbc1f233e9b180f061'\) { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink\('composer-setup.php'\); } echo PHP\_EOL;"
   * php composer-setup.php
   * php -r "unlink\('composer-setup.php'\);"
5. Install composer dependencies:
   * cd lib/pkp
   * php ../../composer.phar --no-dev install
   * cd ../../plugins/paymethod/paypal
   * php ../../../composer.phar --no-dev install
   * cd ../../../plugins/generic/citationStyleLanguage
   * php ../../../composer.phar --no-dev install
6. Install Node.js dependencies \(NOTE: npm must be installed on the server\):
   * cd ../../..
   * npm install
   * npm run build 
7. Create a new config file:
   * cd ../../..
   * cp config.TEMPLATE.inc.php config.inc.php

At this point you should have a fully prepared OJS 3.1 system and database ready to go.  
  


