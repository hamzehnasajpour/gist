### Device registration

```bash
su -
guix package -i px-device-identity px-device-identity-service
px-device-identity -o INIT -s DEFAULT -r REGISTRATION_TERMINAL -a https://idp-server.ones-now.com -dn onesid1.com --force True
```
* Registration should be approved and then DONE.
* Now you can run `px-device-identity-service`

### Websites
* https://vhh-server.ones-now.com
* 
