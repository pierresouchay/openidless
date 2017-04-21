# openidless

A state and backend-less OAuth2 implementation using JWK and JWT.

Most OAuth Servers are complicated to deploy and require databases.

OpenIDless uses JWT tokens only to perform all operations, meaning that while respecting OAuth2 protocol (and OpenID extensions), it is fully stateless and can be deployed in very lightweights environments where you basically only have an LDAP server.

## Goals

Keep it simple, efficient and fast.

### Main Goals

* Use JWK in order to use rotating keys for secrets since all secrets are known after a few hours.
* Use JWT for all inter-application communications and OAuth2 protocol.
* Very simple to deploy from scratch: in 10 minutes!
* Generic and plugable modules to replace all components easily
* Horizontally scalable
* Damn Fast!

### First available modules

* LDAP Connector for authentication: by default, a LDAP implementation is provided with OpenLDAP/OpenDJ/Active Directory Support and Kerberos (optional)
* Plugable Grant System
* Open-bar OAuth2 clients for wildcard URLs (for instance to use internally in your company) 
* Read-Only JWK implementation

### Future

* Full implementation of a JWK server

Provide a plugable system where anybody can use its authentication system. 

