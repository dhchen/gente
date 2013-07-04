## Description
Gente is a web application for self-service LDAP password changes.

## Usage
Gente is configured by editing the values in gente.json. All four entries are mandatory.

  * server: the domain name of your LDAP server 
  * dn: the distinquised name of your users' parent entry in your LDAP tree
  * cafile: the certificate used to validate your LDAP server during TLS negotiation. Leave it empty if your LDAP server doesn't use TLS.
  * title: the name of your gente installation as seen by your users

Gente is written in Perl using the excellent mojolicious framework. Mojolicious supports running as a CGI script or through hypnotoad, its built-in web server. Mojolicious also supports PSGI, which lets you run gente via modperl, FastCGI, SCGI, or any PSGI application server. See the [mojolicious documentation](http://mojolicio.us/perldoc) for more information. There is an example configuration for running Gente via CGI in gente-apache2.markdown

## Requirements
  * Mojolicious
  * Net::LDAP
  * Net::LDAP::Extension::SetPassword
