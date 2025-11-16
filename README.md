# Corne Layout

Keyboard is the [Corne Choc Pro from Keebart](https://www.keebart.com/de/produkte/corne).

## Layers

*Layer 0*

![Layer 0](/images/Layer_0.png)

*Layer 1*

![Layer 1](/images/Layer_1.png)

*Layer 2*

![Layer 2](/images/Layer_2.png)

*Layer 3*

![Layer 3](/images/Layer_3.png)

*Layer 4*

![Layer 4](/images/Layer_4.png)

*Layer 5*

![Layer 5](/images/Layer_5.png)


## Configure the device

- [Vial Konfigurator](https://vial.rocks/) (Only works for chromium based browsers)
- [Keymap Tester](https://usevia.app/test)

### Allow device access on linux

Under Linux you have to modify the permissions for the keyboard. This only works for the web editor.

1. Open chrome://device-log
2. Somewhere will be an error message like
```
Failed to open '/dev/hidraw<device-number>': FILE_ERROR_ACCESS_DENIED
```
3. Execute the following command
```sh
sudo setfacl -m "u:${USER}:rw" /dev/hidraw<device-number>
```
4. Refresh https://vial.rocks/
5. To remove the permission reboot or unplug the device or execute the following command
```sh
sudo setfacl -x "u:${USER}" /dev/hidraw<device-number>
```
