Version: 3.4.2

# 1. Generate the backup
mongodump -d [db-name] -o ~/path/backup/

# 2. Using mongorestore
mongorestore -d [db-name] ~/path/backup/


about the mongoid is created
https://stackoverflow.com/questions/24355927/which-algorithm-does-mongodb-use-for-id
