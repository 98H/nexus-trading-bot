# Deployment & Operations Guide: Trading Bot

## 🚀 Live Access & URLs
- **Live Public Access URL:** [/preview/prod-trading-bot-63f81f/](/preview/prod-trading-bot-63f81f/)
- **Internal Port:** `0`
- **Runtime Engine:** `python_preview`
- **Deployment Status:** `DEPLOYED / ACTIVE`
- **Timestamp:** `2026-09-19T16:14:51.713294+00:00`

## 🛠️ Management & Service Control
### Launch Command
```bash
python3 app.py --port 0
```

### Health Check Probe
```bash
curl -I http://127.0.0.1:0/
```

### Systemd Service Template
```ini
[Unit]
Description=Trading Bot Service
After=network.target

[Service]
Type=simple
WorkingDirectory=/tmp/pytest-of-root/pytest-0/test_scoped_chat_endpoints0/repo/workspaces/prod-trading-bot-63f81f
ExecStart=/usr/bin/python3 /tmp/pytest-of-root/pytest-0/test_scoped_chat_endpoints0/repo/workspaces/prod-trading-bot-63f81f/app.py
Restart=always
RestartSec=3

[Install]
WantedBy=multi-user.target
```

## 🔒 Production Security Protocols
- HTTP-only reverse proxy via Nexus Gateway.
- Dedicated port allocation with zero port conflict.
