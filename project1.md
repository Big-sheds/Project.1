## STEP 1 — INSTALLING APACHE AND UPDATING THE FIREWALL

### Update the list of packages in the package manager
`sudo apt update`

### Install the apache2 package
`sudo apt install apache2`

### Verify if the apache service is running
`sudo systemctl status apache2`

![Apache-status](./images/Capture.PNG)

![Apache-status](./images/Capture2.PNG)

We need to open TCP port 80 which is the default port that web browsers use to access web pages on the Internet.
So we need to add a rule to EC2 configuration to open inbound connection through port 80:

![Apache-status](./images/Capture3.PNG)
Our server is running and we can access it locally and from the Internet.

**Try to access the server from our shell Run ;**

` curl http://localhost:80`

or 

` curl http://127.0.0.1:80`



**Access your Webserver using the url below:**

`http://<Public-IP-Address>:80`

**It should display:**

![Apache-status](./images/Capture4.PNG)


## STEP 2 — INSTALLING MYSQL

We need to install a Database Management System (DBMS) to be able to store and manage data for your site in a relational database. So we Install MYSQL by running ;

`sudo apt install mysql-server`