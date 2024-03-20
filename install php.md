# On Amazon Linux, use yum:
sudo yum install php
sudo yum install php-mbstring
sudo yum install php-intl
sudo yum install php-gd

# Next, download and uncompress the Drupal software by running the following commands in your terminal:
wget https://www.drupal.org/download-latest/tar.gz
tar -xzf tar.gz
mv drupal-* drupal

# If you run “ls” to view the contents of your directory, you will see a tar file and a directory called drupal with the uncompressed contents.
ls

# Change into the drupal directory and copy the files into the Apache root using the following commands.
cd drupal
sudo rsync -avz . /var/www/html
sudo chown -R apache:apache /var/www/html

# Then, restart the Apache service
sudo service httpd restart
