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

### curl commands
```bash
curl -X GET "https://vhh-server.ones-now.com/api/iot-devices/data?filtersList=createdByUser.id~4c660791-6e39-4611-94f3-9dfe5afdf015&relations=createdByUser&timestamps=from~1708517421,to~1708517425" \
     -H "Accept: application/json" \
     -H "Authorization: Bearer yAAAAAQSpS8VTrhVdGr6qdyhXJfwaE1zwD7CI-Z1TYK6ISu" \
     -H "Content-Type: application/json"
```
