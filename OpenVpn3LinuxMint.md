# Tutorial de comandos mas usados en Linux con OpenVpn

## Descarga de OpenVpn3 en Linux

-[OpenVpn 3 Client for Linux](https://openvpn.net/cloud-docs/owner/connectors/connector-user-guides/openvpn-3-client-for-linux.html)


```ruby
$ curl -fsSL https://swupdate.openvpn.net/repos/openvpn-repo-pkg-key.pub | gpg --dearmor | sudo tee /etc/apt/trusted.gpg.d/openvpn-repo-pkg-keyring.gpg

$ DISTRO=$(lsb_release -c | awk '{print $2}')
```

```ruby
$ sudo curl -fsSL https://swupdate.openvpn.net/community/openvpn3/repos/openvpn3-$DISTRO.list -o /etc/apt/sources.list.d/openvpn3.list

$ sudo apt update

$ sudo apt install openvpn3
```

```ruby
$ openvpn3 session-start --config ${MY_CONFIGURATION_FILE}
```

```ruby
$ openvpn3 sessions-list
$ openvpn3 session-manage --session-path /net/openvpn/v3/sessions/..... --disconnect
```