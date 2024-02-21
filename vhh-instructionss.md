### Device registration

```bash
su -
guix package -i px-device-identity px-device-identity-service
px-device-identity -o INIT -s DEFAULT -r REGISTRATION_TERMINAL -a https://idp-server.ones-now.com -dn onesid1.com --force True
```
