= Leaving the cloud =

Couple of notes on an ongoing project of setting up my networking
environment on own server.

* Postfix SMTP server configured.
* Dovecot for IMAP access.
* SASL authentication via Dovecot in Postfix, TLS support in Postfix
* msmtp at notebook for outgoing emails from Mutt
* mutt at notebook
* Roundcube at the server for eventual web access to the mail from other than
  my notebook (https access via self-signed key)
* OpenLDAP at the server and configured as the address book for the Roundcube
* Google contacts imported via Roundcube (vCard format)
* address tab completion in mutt using an LDAP search script located at the
  server and executed remotely via ssh (so that I do not need to open the LDAP
  port)
* Gitlab via Apache/Passenger
* prosody.im with self-signed TLS certificate
  * Note: In the dark past, I was experimenting with the Google Apps for my
    domain. Never actually started to use it so Google de-activated it
    themselves. However, when setting up XMPP for my domain, gmail.com accounts
    were unable to contact it and I got
    *Session closed by remote with error: undefined-condition (mudrak.name is a
    Google Apps Domain with Talk service enabled.)*
    in my prosody.log. Shutting down the Google Apps for the domain solved the
    trouble immediately.
