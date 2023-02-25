# **MEAN STACK DEPLOYMENT TO UBUNTU IN AWS**

## Step 1: Install NodeJs

* **updated ubuntu with the code below**

`sudo apt update` 
![sudo update](./images/sudo%20update.PNG)

* **upgraded ubuntu with the code below**

`sudo apt upgrade`

![sudo upgrade](./images/sudo%20upgrade.PNG)

* **added certicates with the code below**

`sudo apt -y install curl dirmngr apt-transport-https lsb-release ca-certificates`

`curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -`

![add cert](./images/add%20cert.PNG)

* **installed node.js with the code below**

`sudo apt install -y nodejs`

![apt node.js](./images/apt%20node.js)

## Step 2: Install MongoDB

![step](./images/step.PNG)

![mongodb](./images/mongodb.PNG)

![mongodb2](./images/mongodb%202.PNG)

* **installed mongodb with the code below**

![apt mongodb](./images/apt%20mongodb.PNG) 

* **started and verify the server is running with the codes belwo**

`sudo service mongodb start`

`sudo systemctl status mongodb`

![start & status](./images/start%20%26%20status.PNG)

* **Installed npm – Node package manager with the code below**

`sudo apt install -y npm`

* I**nstalled body-parser package with the code below**

`sudo npm install body-parser`

![mong](./images/mong.PNG)


* **followed the step below**


![step1](./images/step1.PNG)

![init](./images/init.PNG)

* **Add a file to it named server.js**

![v1](./images/vi%201.PNG)

* **continuatiom**

![step2](./images/step%202.PNG)

![v2](./images/vi%202.PNG)

* **continuation**

![step3](./images/step3.PNG)

![v3](./images/vi%203.PNG)

![step4](./images/step4.PNG)

![v4](./images/vi%204.PNG)


## FINALLY  I CREATED A **INDEX.HTML FILE**  INPUTTED THE REQUIRE CODE IN IT, WENT BACK TO THE **BOOKS DIRECTORY** THEN STARTED THE SERVER BY RUNNING THE CODE `node server.js` 


![web](./images/web%201.PNG)