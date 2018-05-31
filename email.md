# Email

**Primary and Technical Contacts**

All PKP applications require that a primary and technical contact are configured under Setup for proper  daily operations. This has to be done for every journal, press or conference on the system. In OJS 2.x, this can be done under _Setup Step 1_. In OCS 2.x, this can be done under _Website Management Step 1_. IN OJS/OMP 3.x, this can be done under _Settings &gt; Journal &gt; Contact_.

**Sending Mail**

By default, mail is sent through PHP's built-in `mail()` facility.

On Windows, PHP needs to be configured to send email through a SMTP server \(running either on the same machine or on another machine\).

On other platforms such as Linux and Mac OS X, PHP will sent mail using the local sendmail client, so a local MTA such as Sendmail or Postfix must be running and configured to allow outgoing mail.

See [http://www.php.net/mail](http://www.php.net/mail) for more details on configuring PHP's mail functionality.

Our software can also be configured to use an SMTP server as specified in `config.inc.php`, either with or without authentication.



More here still needs to be written. Will include information on: 

* Setting up envelope\_sender etc.
* SMTP stuff
* configuring and troubleshooting



