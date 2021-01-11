## Requires a working Ubuntu setup under WSL

# Install the Service
sudo apt update
sudo apt install postgresql postgresql-contrib

# Start the Service
sudo service postgresql start

# Create a sample db (text in <> brackets indicates a value that you choose.  the brackets should be left out)
sudo -u postgres psql
create database <dbname>;

# Create a user and grant permissions (text in <> brackets indicates a value that you choose.  the brackets should be left out)
create user <username> with encrypted password '<password>';
grant all privileges on database <dbname> to <username>; 

# Going Forward
When starting the Ubuntu shell, you will need to start the service using sudo service postgresql start
