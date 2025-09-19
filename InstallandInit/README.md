# 📚 PostgreSQL Installation & Verification Guide

This guide documents the process of installing PostgreSQL, starting the service, locating key directories, and verifying the installation.

---

## ✅ 1. Install PostgreSQL

### For Ubuntu/Debian:
```bash
sudo apt update
sudo apt install postgresql postgresql-contrib -y
For RHEL/CentOS:
sudo yum install postgresql-server postgresql-contrib -y
sudo postgresql-setup initdb
________________________________________
✅ 2. Enable & Start PostgreSQL Service
sudo systemctl enable --now postgresql
sudo systemctl status postgresql
📸 Screenshot:
 
________________________________________
✅ 3. Locate Configuration & Data Directories
Find Config Directory:
pg_config --sysconfdir
📸 Screenshot:
 
________________________________________
Find Data Directory:
Connect to PostgreSQL:
sudo -u postgres psql
Inside psql run:
SHOW data_directory;
\q
📸 Screenshot:
 
________________________________________
✅ 4. Connect & Verify PostgreSQL Version
Connect:
sudo -u postgres psql
Check version:
SELECT version();
\q
📸 Screenshot:
 
________________________________________
📂 Folder Structure
Your repository should look like this:
.
├── README.md
└── screenshots
    ├── service-status.png
    ├── config-dir.png
    ├── data-dir.png
    └── version.png
________________________________________
🎯 Deliverable Checklist
•	 Installed PostgreSQL
•	 Enabled & started service
•	 Located config & data directories
•	 Connected to psql & verified version
•	 Captured & added screenshots in screenshots/ folder
________________________________________

