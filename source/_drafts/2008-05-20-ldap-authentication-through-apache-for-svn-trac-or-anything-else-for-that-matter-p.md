---
title: >-
  LDAP authentication through Apache for svn, trac or anything else for that
  matter :P
author: Sahil Ahuja
categories: blog
tags:
  - apache
  - delta
  - fedora
  - httpd
  - ldap
  - pragyan
  - svn
  - trac
id: 33
date: 2008-05-20 02:07:00
---

Apache can be used as an access method for things like svn, trac, and even a whole file system through webdav. And apache also supports authentication through LDAP. Hence Apache can be used to authenticate the services that it provides through LDAP.

Here is how it is done :

**For SVN :**

`&lt;VirtualHost *:80&gt;
ServerName                          repos.nitt.edu
DocumentRoot                        "/var/www/svn/DocumentRoot/"
ErrorLog logs/repos.nitt.edu-error_log
CustomLog logs/repos.nitt.edu-access_log combined`

&lt;Location /pragyan&gt;
DAV svn
SVNPath /var/www/svn/pragyan
&lt;LimitExcept OPTIONS REPORTGET&gt;
AuthType Basic
AuthBasicProvider ldap
AuthzLDAPAuthoritative off
AuthName "Pragyan SVN LDAP Authentication"
AuthLDAPURL ldap://localhost:389/ou=Pragyan,dc=www,dc=nitt,dc=edu?cn?sub?(objectClass=*)
AuthLDAPGroupAttribute contact
require valid-user
require ldap-group listName=coding,ou=Groups,ou=Pragyan,dc=www,dc=nitt,dc=edu
&lt;/LimitExcept&gt;
&lt;/Location&gt;
&lt;/VirtualHost&gt;

**For trac :**
`&lt;Location "/trac/delta/login"&gt;
AuthType Basic
AuthName "Delta Trac LDAP Authentication"
AuthBasicProvider ldap
AuthzLDAPAuthoritative off
AuthLDAPURL ldap://delta.nitt.edu:389/ou=Webteam,dc=delta,dc=nitt.edu?uid?sub?(objectClass=*)
AuthLDAPGroupAttribute memberUid
require valid-user
require ldap-group cn=webteam,ou=Groups,ou=Webteam,dc=delta,dc=nitt.edu
&lt;/Location&gt;`