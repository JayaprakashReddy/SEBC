```
[kdcdefaults]
 kdc_ports = 88
 kdc_tcp_ports = 88

[realms]
 JAYAPRAKASHREDDY.SG = {
  #master_key_type = aes256-cts
  acl_file = /var/kerberos/krb5kdc/kadm5.acl
  dict_file = /usr/share/dict/words
  admin_keytab = /var/kerberos/krb5kdc/kadm5.keytab
  supported_enctypes = aes256-cts-hmac-sha1-96:normal aes128-cts-hmac-sha1-96:normal des3-hmac-sha1:normal arcfour-hmac-md5:normal
  max_renewable_life = 7d
 }
```