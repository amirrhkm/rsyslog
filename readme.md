## Rsyslog Configuration and Capabilities

### Installation

```bash
apt install rsyslog -y
```

### Open Ports

```bash
ufw allow 514/tcp
ss -tuln | grep 514
```

### Configuration

- `server/rsyslog.conf` - Configuration for the server
- `client/rsyslog.conf` - Configuration for the client
