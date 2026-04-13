First of all, make sure to enable the firewall. This can be done in the Plasma System Settings or the corresponding for other desktop environments. Alternatively, in the terminal (as root):
```
ufw enable
```

When the firewall is enabled and if you are using LocalSend, you will discover that LocalSend does not work. To make it work, we need to open a port. Run the following commands in a terminal (as root):
```
ufw allow 53317/tcp
ufw allow 53317/udp
```

These commands open the port 53317 over protocols TCP and UDP. This is the default port used by LocalSend.

**Useful sources:**
- [https://github.com/localsend/localsend/issues/1230](https://github.com/localsend/localsend/issues/1230)
- [https://help.ubuntu.com/community/UFW](https://help.ubuntu.com/community/UFW)