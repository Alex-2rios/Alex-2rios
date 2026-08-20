## Alex Rios Carballo

Computer Systems Engineering student. Cisco certified. Most of what I build ends up being
infrastructure: servers, containers, networks, and the small machines that report back to them.

I like the parts of a system that only show up when something breaks. Load balancers are
interesting the moment a backend dies, backups are interesting the day you have to restore one,
and an alert rule is worth nothing until you have watched it fire on purpose.

### What I work with

| | |
|---|---|
| **Networking** | subnetting and VLSM, routing and switching, ACLs, VLANs, Cisco IOS |
| **Linux and infrastructure** | Docker and Compose, NGINX, HAProxy, SSH hardening, UFW, systemd, bash |
| **Monitoring** | Prometheus, Grafana, Alertmanager, node exporter, blackbox probes |
| **Embedded** | ESP32, C++ with the Arduino framework, sensor interfacing, state machines |
| **Backend** | Python, FastAPI, Flask, PostgreSQL, MySQL, JWT auth, pytest |
| **Mobile and web** | React Native with Expo, JavaScript, HTML and CSS |

### Things I have built

- **Terracota** — point of sale for a café: one FastAPI service, a React Native app for waiters,
  kitchen and cashier, a Flask admin panel and PostgreSQL underneath. Deployed behind TLS, and
  no client ever touches the database.
- **Homelab monitoring** — Prometheus, Grafana and Alertmanager watching my own machines, with
  eleven alert rules and a script that breaks something on purpose to prove they fire.
- **High availability web stack** — NGINX terminating TLS in front of HAProxy and two backends.
  Killing a backend mid traffic costs zero failed requests, which I measured rather than assumed.
- **Bastion host lab** — one reachable machine, everything else on a network with no route out,
  and eight checks that assert the blocked paths are actually blocked.
- **ESP32 sensor node** — firmware that samples temperature, humidity and light and serves its
  own dashboard over WiFi, no cloud involved.

### Right now

Studying for the next Cisco exam, and slowly turning my homelab into something that pages me
before I notice a problem instead of after.

Reach me at rioscarballoa@gmail.com.
