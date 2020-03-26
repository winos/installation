Version: 3.4.2

# 1. Generate the backup
mongodump -d [db-name] -o ~/path/backup/

# 2. Using mongorestore
mongorestore -d [db-name] ~/path/backup/
