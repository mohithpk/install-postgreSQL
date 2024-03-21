# Step 1: Update AL2023 Packages
. sudo dnf update

# Step 2: Install PostgreSQL 15 on Amazon Linux 2023
. sudo dnf install postgresql15.x86_64 postgresql15-server

# Step 3: Initialize the PostgreSQL Database
. sudo postgresql-setup --initdb

# Step 5: Add the PostgreSQL service to the system startup.
. sudo systemctl start postgresql

# Step 6: Check the status of PostgreSQL using the following command.
. sudo systemctl status postgresql
