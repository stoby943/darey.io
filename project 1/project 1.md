# WEB STACK IMPLEMENTATION (LAMP STACK) IN AWS

## **so to implement our lamp stack we have to firstly**

* Install apache and update firewall

Install Apache using Ubuntu’s package manager ‘apt’:


             #update a list of packages in package manager using the command below   
             
 `sudo apt update`

 ![sudo apt update](./images/sudo%20apt%20update.PNG)

   
             #run apache2 package installation using the command below
`sudo apt install apache2`

![sudo apt install apache2](./images/sudo%20apt%20install%20apache2.PNG)


* verify if our apache2 is running on our OS with the command below 

`sudo systemctl status apache2`

![sudo systemct1 status apache2](./images/sudo%20systemctl%20status%20apache2.PNG)



## the next thing to do is go to your aws ............
## add a rule to EC2 configuration to open inbound connection through port 80: by
* click on your instance to show your details
* go to network and find security groups
* click on impound rules 
* click on edit impound rules
* click on add rules        


        # TYPE: custom tcp     PROTOCOL: tcp    PORT RANGE: 80  SOURCE: custom 
        
        configure your impound rules like this 

* save rules 



## then try to check if we can access it locally  our ubuntu why using the command below
`curl http://localhost:80`


## test how our Apache HTTP server can respond to requests from the Internet.
Open a web browser of your choice and try to access following url
inputting your ip address where public-ip-address is written

 `http://<Public-IP-Address>:80`

## **NEXT STEP IS TO INSTALL MYSQL**
Again, use ‘apt’ to acquire and install this software:

`sudo apt install mysql-server`

When prompted, confirm installation by typing Y, and then ENTER.


![sudo apt install mysql-server](./images/sudo%20apt%20install%20mysql-server.PNG)

When the installation is finished, log in to the MySQL console by typing:

`sudo mysql`

![sudo mysql](./images/sudo%20mysql.PNG)


It’s recommended that you run a security script that comes pre-installed with MySQL. This script will remove some insecure default settings and lock down access to your database system. Before running the script you will set a password for the root user, using mysql_native_password as default authentication method. We’re defining this user’s password as Oladiph99%


`ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'Oladiph99%';`



    mysql> ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'Oladiph99%';
     Query OK, 0 rows affected (0.01 sec)



Exit the MySQL shell with:

`mysql> exit`

Start the interactive script by running

 `sudo mysql_secure_installation`


 This will ask if you want to configure the VALIDATE PASSWORD PLUGIN
                
                VALIDATE PASSWORD PLUGIN can be used to test passwords
                and improve security. It checks the strength of password
                and allows the users to set only those passwords which are
                secure enough. Would you like to setup VALIDATE PASSWORD plugin?

                Press y|Y for Yes, any other key for No:

If you answer “yes”, you’ll be asked to select a level of password validation

               there are three levels of password validation policy:

               LOW    Length >= 8
               MEDIUM Length >= 8, numeric, mixed case, and special characters
               STRONG Length >= 8, numeric, mixed case, special characters and 
               dictionary              file

               Please enter 0 = LOW, 1 = MEDIUM and 2 = STRONG: 1

If you are happy with your current password, enter Y for “yes” at the prompt:

      Estimated strength of the password: 100 
      Do you wish to continue with the password provided?(Press y|Y for Yes, any 
      other key for No) : y

When you’re finished, test if you’re able to log in to the MySQL console by typing:

`sudo mysql -p`

![sudo mysql -p](./images/sudo%20mysql%20-p.PNG)



