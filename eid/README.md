# Archlinux Belgian eID Omnikey Card Reader 

Belgian eID Omnikey card reader installation for Chrome and Firefox

## Installation

Install theses packages

```bash
sudo pacman -S pcsclite ccid opensc --noconfirm --needed
```

Card reader driver [Omnikey ifdokccid](https://aur.archlinux.org/packages/omnikey_ifdokccid)

Tools
- about-eid-mw 
- eid-env 
- eid-viewer

### Chrome

Install [nss](https://wiki.archlinux.org/title/Network_Security_Services)

Add device to Chrome

```bash 
modutil -dbdir sql:.pki/nssdb -add "Belgium eID" -libfile
/usr/lib/libbeidpkcs11.so 
```

### Firefox

Go to your Privacy & Security settings
[Preferences Privacy](about:preferences#privacy) then to `Security`,
`Certificates` and click on `Security Devices...`

In the Device Manager window click the `Load` button.  ´New PKCS#11 Module´


## References

[Archlinux - Electronic identification](https://wiki.archlinux.org/title/Electronic_identification)
[Archlinux - Omnikey Cardman](https://wiki.archlinux.org/title/Omnikey_Cardman_5321)
[Firefox - Add card reader](https://eid.belgium.be/fr/faq/firefox-comment-installer-et-activer-le-module-complementaire-eid#7311)
[](https://eid.belgium.be/en/log-eid#7504)
