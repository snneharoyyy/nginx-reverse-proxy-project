
## 🚀 How It Works

- `http://localhost/app1/` → App 1 (Port 5000)
- `http://localhost/app2/` → App 2 (Port 5001)

NGINX acts like a **traffic controller**, routing user requests to the correct app based on the URL path.

## ⚙️ How to Run This

1. Start two HTTP servers:
    ```bash
    cd app1 && python3 -m http.server 5000
    cd app2 && python3 -m http.server 5001
    ```

2. Copy the NGINX config:
    ```bash
    sudo cp nginx-config/default /etc/nginx/sites-available/default
    sudo systemctl restart nginx
    ```

3. Visit in your browser:
    - `http://localhost/app1/`
    - `http://localhost/app2/`

## 🧠 Concepts Used

- NGINX reverse proxy
- HTTP servers
- Networking (ports, localhost)
- Git & GitHub version control
- Markdown documentation

## 🛠 Built With

- [NGINX](https://nginx.org/)
- [Python HTTP Server](https://docs.python.org/3/library/http.server.html)
- [GitHub](https://github.com/)

---

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
