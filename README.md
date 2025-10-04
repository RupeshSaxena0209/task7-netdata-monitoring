# Task 7 - Monitor System Resources Using Netdata

## 📌 Objective
Install and run **Netdata** to visualize system and application performance metrics in real-time.

---

## ⚙️ Tools Used
- **Docker**
- **Netdata** (open-source monitoring tool)

---

## 🚀 Steps to Complete

### 1. Run Netdata Container
Make sure Docker is installed and running, then execute:

```bash
docker run -d --name=netdata   -p 19999:19999   --cap-add=sys_ptrace   --security-opt apparmor=unconfined   netdata/netdata
```

---

### 2. Access the Dashboard
- Open browser → [http://localhost:19999](http://localhost:19999)  
- The dashboard shows real-time CPU, memory, disk, network, and Docker container metrics.

---

### 3. Explore Metrics
- **CPU Usage** – per-core utilization
- **Memory Usage** – RAM consumption
- **Disk I/O** – read/write speed
- **Docker Containers** – container performance
- **Network Traffic** – incoming/outgoing bandwidth

---

### 4. Logs
Check logs of Netdata:
```bash
docker logs netdata
```
or inside the container:
```bash
docker exec -it netdata bash
cat /var/log/netdata/error.log
```
---
