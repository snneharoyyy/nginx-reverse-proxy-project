# NGINX Reverse Proxy Project

This project demonstrates how to set up NGINX as a reverse proxy to route traffic to two local HTTP servers.

## Structure
- `/app1/` → forwards to port 5000
- `/app2/` → forwards to port 5001

## How to Run
1. Start two servers:
   ```bash
   python3 -m http.server 5000
   python3 -m http.server 5001
