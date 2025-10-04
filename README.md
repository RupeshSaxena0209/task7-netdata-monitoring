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

### 5. Screenshots
Add screenshots from the dashboard:
- `dashboard.png` → Full Netdata dashboard
- `cpu_memory.png` → CPU & memory usage
- `docker_metrics.png` → Docker containers monitoring

---

### 📊 Outcome
- Successfully deployed Netdata via Docker
- Visualized **real-time system metrics**
- Understood **lightweight monitoring** for servers & containers

---

## ❓ Interview Questions & Answers

1. **What does Netdata monitor?**  
   → CPU, RAM, disk, network, Docker containers, applications, logs.

2. **How to view real-time metrics?**  
   → Via dashboard at `http://localhost:19999`.

3. **How is Netdata different from Prometheus?**  
   → Netdata provides real-time visual dashboards automatically, while Prometheus is a time-series database requiring manual setup and Grafana for visualization.

4. **What is a collector?**  
   → A plugin/module in Netdata that gathers specific metrics (CPU, memory, MySQL, Docker, etc.).

5. **What KPIs are important?**  
   → CPU load, memory usage, disk I/O, network latency, container health.

6. **How to deploy on VM?**  
   ```bash
   bash <(curl -Ss https://my-netdata.io/kickstart.sh)
   ```

7. **How does Netdata alerting work?**  
   → It has built-in health checks and configurable alarms with notifications (email, Slack, etc.).

8. **What is a dashboard?**  
   → A web UI showing real-time performance metrics using charts and alerts.

---

## 📤 Submission
- Upload repo to GitHub  
- Include README.md and screenshots  
- Submit repo link via: [Google Form](https://forms.gle/qumsSk73uxUZ6LYB9)

---

✅ **Task Completed**
