# PostgreSQL Installation & Verification

## 1. Install PostgreSQL
```bash
sudo apt update
sudo apt install postgresql postgresql-contrib -y

# 2. Enable & Start PostgreSQL Service
sudo systemctl enable --now postgresql
sudo systemctl status postgresql


# 3. Locate Config & Data Directories
pg_config --sysconfdir


Inside psql:

SHOW data_directory;


# 4. Connect & Verify Version
sudo -u postgres psql
SELECT version();



---
