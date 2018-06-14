User Stories
============

Initialise a new CA
-------------------

```
minica init --database=/secure/vpn_ca --profile=x509_vpn \
    --dn="o=vpn_ca, cn=ca 1" \
    --base_dn="o=vpn_ca"
```

Add a principal
---------------

```
minica add host.example.com --san="ip:192.0.2.1" --san="ip6:[2001:db8:1:1::1]"
```

Renew certificate
-----------------

```
minica renew host.example.com --force --no-revokation
```

Report on active certificates and their expiry
----------------------------------------------

Revoke a certificate
--------------------

```
minica revoke -f cert.der
```

List/search principals
----------------------

```
minica list *.example.com
```