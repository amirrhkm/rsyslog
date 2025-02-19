## Rsyslog Configuration and Capabilities

### Installation

```bash
apt install rsyslog -y
```

### Common Commands

```bash
ufw allow 514/tcp
ss -tuln | grep 514
sysctl -w vm.max_map_count=262144
```

### Configuration

- `server/rsyslog.conf` - Configuration for the server
- `client/rsyslog.conf` - Configuration for the client
