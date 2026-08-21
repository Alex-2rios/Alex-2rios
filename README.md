## Alex Ríos Carballo

Computer Systems Engineering student. Cisco certified. Most of what I build ends up being
infrastructure: servers, containers, networks, and the small machines that report back to them.

I like the parts of a system that only show up when something breaks. A load balancer is
interesting the moment a backend dies, a backup is interesting the day you have to restore one,
and an alert rule is worth nothing until you have watched it fire on purpose. So the repositories
below all have the same shape: build the thing, then break it and measure what happened.

### What I work with

| | |
|---|---|
| **Networking** | subnetting and VLSM, routing and switching, ACLs, VLANs, Cisco IOS |
| **Linux and infrastructure** | Docker and Compose, NGINX, HAProxy, SSH hardening, UFW, Ansible, systemd |
| **Monitoring** | Prometheus, Grafana, Alertmanager, exporters, alert rules and runbooks |
| **Embedded** | ESP32, C++ with the Arduino framework, sensor interfacing, state machines |
| **Backend** | Python, FastAPI, Flask, PostgreSQL, MySQL, JWT auth, pytest |
| **Mobile and web** | React Native with Expo, JavaScript, HTML and CSS |

### Things I have built

**[terracota-restaurant-system](https://github.com/Alex-2rios/terracota-restaurant-system)** —
point of sale for a café. One FastAPI service, a React Native app for waiters, kitchen and
cashier, a Flask admin panel and PostgreSQL underneath. No client ever touches the database, and
PostgreSQL error codes are translated into HTTP status codes so a caller can tell a duplicate
from a real fault.

**[homelab-monitoring](https://github.com/Alex-2rios/homelab-monitoring)** — Prometheus, Grafana
and Alertmanager watching my own machines. Sixteen alert rules, unit tested with `promtool`, each
one linked to a runbook. A drill stops an exporter on purpose and measures the detection window
instead of assuming it.

**[ha-web-infrastructure](https://github.com/Alex-2rios/ha-web-infrastructure)** — NGINX
terminating TLS in front of HAProxy and two backends. Killing a backend mid traffic costs zero
failed requests, and that number comes from a script, not from a diagram.

**[bastion-host-lab](https://github.com/Alex-2rios/bastion-host-lab)** — one reachable machine,
everything else on a subnet with no route out. Nine checks, five of which assert that something
is blocked, plus an Ansible playbook that applies the same hardening to real hosts.

**[network-toolkit](https://github.com/Alex-2rios/network-toolkit)** — subnetting, VLSM planning,
host discovery and a connectivity test that tells you which layer is broken. No dependencies,
90% test coverage.

**[esp32-sensor-node](https://github.com/Alex-2rios/esp32-sensor-node)** and
**[esp32-inspection-fsm](https://github.com/Alex-2rios/esp32-inspection-fsm)** — firmware where
the logic lives in a library with no Arduino headers, so the state machine and the telemetry
buffer are unit tested on a laptop with no board attached.

Every one of them builds in CI on each push, gets scanned for secrets and vulnerable
dependencies weekly, and has a README that says what broke while I was building it.

### Right now

Studying for the next Cisco exam, and slowly turning my homelab into something that pages me
before I notice a problem rather than after.

Reach me at rioscarballoa@gmail.com.
