# PortMapper-Go
A lightweight port mapping/forwarding/relaying utility written in Go

### Features
- Support domain as target address
- Small size, single executable
- Support traffic limit(max speed/ burst speed/ data caps)

### Running
```
# TCP Only
./portmapper -l 0.0.0.0:3389 -r example.com:3389 -t

# both TCP and UDP
./portmapper -l 0.0.0.0:3389 -r 192.168.1.2:3389 -t -u

# both TCP and UDP, maxmium speed 10Mbps, burst speed 20Mbps, data cap 1GB
./portmapper -l 0.0.0.0:3389 -r 192.168.1.2:3389 -t -u -rate 10 -burst 20 -cap 1GB
```