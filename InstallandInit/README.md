# 📚 PostgreSQL Installation & Verification Guide

This guide documents the process of installing PostgreSQL, starting the service, locating key directories, and verifying the installation.

---

## ✅ 1. Install PostgreSQL

### For Ubuntu/Debian:
```bash
```
```
sudo apt update
sudo apt install postgresql postgresql-contrib -y
```
For RHEL/CentOS:
```
sudo yum install postgresql-server postgresql-contrib -y
sudo postgresql-setup initdb
```
________________________________________
✅ 2. Enable & Start PostgreSQL Service
```
sudo systemctl enable --now postgresql
sudo systemctl status postgresql
```
📸 Screenshot:
 <img width="1167" height="217" alt="Screenshot 2025-09-19 214008" src="https://github.com/user-attachments/assets/dcb41f0e-81c2-4faa-aeb2-6d7635dcb760" />

________________________________________
✅ 3. Locate Configuration & Data Directories
Find Config Directory:
```
pg_config --sysconfdir
```
📸 Screenshot:
 <img width="976" height="530" alt="Screenshot 2025-09-19 220555" src="https://github.com/user-attachments/assets/cdfc5667-08c0-4618-b95d-44e88aa78da2" />

________________________________________
Find Data Directory:
Connect to PostgreSQL:
```
sudo -u postgres psql
```
Inside psql run:
```
SHOW data_directory;
\q
```
📸 Screenshot:
 <img width="612" height="297" alt="Screenshot 2025-09-19 214157" src="https://github.com/user-attachments/assets/090829ba-1c41-41e7-8b2d-6cbaafff3dcf" />

________________________________________
✅ 4. Connect & Verify PostgreSQL Version
Connect:
```
sudo -u postgres psql
Check version:
SELECT version();
\q
```
📸 Screenshot:
 <img width="1694" height="352" alt="Screenshot 2025-09-19 214306" src="https://github.com/user-attachments/assets/b7424c12-a180-448d-a2e3-2f57d5ae7a3d" />
```
________________________________________
🎯 Deliverable Checklist
•	 Installed PostgreSQL
•	 Enabled & started service
•	 Located config & data directories
•	 Connected to psql & verified version
•	 Captured & added screenshots in screenshots/ folder
________________________________________

