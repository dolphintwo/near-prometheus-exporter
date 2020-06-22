# Docker-Compose一键启动Grafana 

- 修改 `etc/prometheus/prometheus.yml`中的`NODE_IP_ADDRESS`
- 修改 `docker-compose.yml`中的`accountId`

## 启动

```bash
docker-compose up -d
```

访问Grafana: `http://localhost:3000`

Username: admin
Password: admin

打开 `Near Exporter` 看板

### 配置邮件告警

修改Grafana配置文件中邮件相关配置 `etc/grafana/custom.ini`

```ini
[smtp]
enabled = true
host = smtp.gmail.com:587 
user = <your_gmail_address>
password = <your_gmail_password>
;cert_file =
;key_file =
skip_verify = true
from_address = <your_gmail_address>
from_name = Grafana
```

## 更新

```bash
git pull
docker-compose build
docker-compose down && docker-compose up -d
```

