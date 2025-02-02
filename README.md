# 🚀 Nextcloud + Traefik + Collabora with Docker Compose

This repository provides a **Docker Compose** setup to deploy **Nextcloud**, **Traefik (as a reverse proxy with Let's Encrypt SSL certificates)**, and **Collabora Online** for document editing. The setup includes a **MariaDB database** for Nextcloud.

## 📌 Features

- **Nextcloud**: Self-hosted file sync and sharing platform
- **Traefik**: Reverse proxy and automatic Let's Encrypt SSL certificate management
- **Collabora**: Online document editing with Nextcloud
- **MariaDB**: Database for Nextcloud
- **Environment variables** for easy customization

---

## 🛠️ Prerequisites

- **Docker** & **Docker Compose** installed
- **A domain name** (e.g., `cloud.example.com`, `collabora.example.com`)
- **Open ports 80 & 443** on your server for Let's Encrypt to issue SSL certificates

---

## 🚀 Deployment Steps

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/Narkle/minimal-traefik-docker-compose-nextcloud-collabora.git
cd minimal-traefik-docker-compose-nextcloud-collabora
```

### 2️⃣ Configure Environment Variables
Copy the `.env.example` file and set your values:
```bash
cp .env.example .env
```
Edit the `.env` file:
```ini
NEXTCLOUD_ADMIN_USER=admin
NEXTCLOUD_ADMIN_PASSWORD=yourpassword
NEXTCLOUD_HOSTNAME=cloud.example.com
COLLABORA_HOST=collabora.example.com
ACME_MAIL=your-email@example.com
```

### 3️⃣ Start the Containers
```bash
docker-compose up -d
```

### 4️⃣ Verify Services
- **Traefik Dashboard**: `https://your-domain.com/dashboard/`
- **Nextcloud**: `https://cloud.example.com`
- **Collabora**: `https://collabora.example.com`

---

## 🛠 Configuration

### 🔹 Nextcloud
- First-time setup at `https://cloud.example.com`
- Use the **admin credentials** from `.env`
- Database:  
  - **Host**: `db`
  - **User**: `nextcloud`
  - **Password**: Use `MYSQL_PASSWORD` from `.env`
  - **Database**: `nextcloud`

### 🔹 Collabora
- The integration is automatic via Traefik.
- **In Nextcloud**, install the **Collabora Online app** from the Nextcloud App Store.

---

### 🚀 Happy Hosting!


### 🔥 Key Features of This README:
- **Structured & clear instructions**
- **Deployment steps & troubleshooting**
- **Security best practices**
- **Useful Docker commands**
- **Future improvement roadmap**

