## Server Setup

Update package Manager upgrade system install wireguard:
```bash
sudo apt update && upgrade
sudo apt install wireguard-tools
```

Login as root and navigate to `/etc/wireguard`

Generate the keys with the command:
```bash
wg genkey | tee privatekey | wg pubkey > publickey
```

Make a file named `wg0.conf` and use the following setup:
```
PrivateKey = _private_key_
Address = 10.0.0.1/24
SaveConfig = true
PostUp = iptables -A FORWARD -i wg0 -j ACCEPT; iptables -t nat -A POSTROUTING -o eth0  -j MASQUERADE
PostDown = iptables -D FORWARD -i wg0 -j ACCEPT; iptables -t nat -D POSTROUTING -o eth0 -j MASQUERADE
ListenPort = 51820
```

Additionally add the following lines to `PostUp` and `PostDown` if you want wireguard to connect out to the internet.
```
; iptables -A FORWARD -o wg0 -j ACCEPT
; iptables -D FORWARD -o wg0 -j ACCEPT
```

Open up the port 51820/udp:
```
ufw enable
ufw allow 51820/udp
ufw reload
```

Start wireguard with:
```
wg-quick up wg0
```

Add a Peer with the following command:
```bash
wg set wg0 peer _public_key_ allowed-ips _allowed_ips_here_
```

## Client Configuration

Install is the same as with [[#Server Setup]] for Linux.

For Windows got to [this](https://www.wireguard.com/install/) link for the installer.

Configuration for the client is also relatively similar to [[#Server Setup]].

The configuration file follows the following format:
```
[Interface]
PrivateKey = _private_key_
Address = _private_ip_addr_
DNS = 1.1.1.1, 1.0.0.1

[Peer]
PublicKey = _server_public_key_
AllowedIPs = 0.0.0.0/0
Endpoint = _server_ip_addr_:51820
```

### Notes:

- On machines hidden behind a NAT (A machine that is on a private network and whose public ip is forwarded to the edge router) you will need to add the following line under the `[Peer]` section to ping to vpn server:
```
PersistentKeepalive = 25
```

- If you set `AllowedIPs` to 0.0.0.0/0 it will route all traffic from the client to the server. However you can specify which addresses you want tunneled in a comma separated list if you only want private ip addresses to be tunneled. e.g.
```
AllowedIPs = 10.0.0.1/24, 10.0.0.2/24, 10.0.0.3/24, ...
```

 - If a network blocks udp traffic you may not be able to use your vpn because wireguard operates on the udp protocol only.

- To setup autoconnect:
```bash
sudo systemctl enable wg-quick@wg0.service
sudo systemctl daemon-reload
sudo systemctl start wg-quick@wg0
```

