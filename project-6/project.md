# **WEB SOLUTION WITH WORDPRESS**

## **i created two instances and  six volumes with a space of 10G each attaching three volumes to each instance**
 
* **used lsblk command to view the attached volume**

![volume attach](./images/volume%20attach.PNG)

* **created partions**

![parti1](./images/parti1.PNG)

![parti2](./images/parti2.PNG)

![parti3](./images/parti3.PNG)

* **installed lvm2 using the code below**

`sudo yum install lvm2`

![yum lvm2](./images/yum%20lvm2.PNG)

* **created physical volumes with pvcreate**

![pv create](./images/pv%20create.PNG)

**verified my created physical volumes with `sudo pvs`**

![pvs](./images/pvs.PNG)


             i performed the steps above on both instances



## **on my client server i created volume group with vgcreate with the code below**

`sudo vgcreate webdata-vg /dev/xvdh1 /dev/xvdg1 /dev/xvdf1`


![vgcreate](./images/vgcreate.PNG)


**verified my volume groups**

![vgs](./images/vgs.PNG)


**created a logical volume with the code below**

`sudo lvcreate -n apps-lv -L 14G webdata-vg`

`sudo lvcreate -n logs-lv -L 14G webdata-vg`

![lv](./images/lv.PNG)
 
**verified my logical volumes**

![lv v](./images/lv%20v.PNG)

**Verify the entire setup**

![vg display](./images/vg%20display.PNG)

**Use mkfs.ext4 to format the logical volumes with ext4 filesystem**

i used the code below to format my logical volumes

`sudo mkfs -t ext4 /dev/webdata-vg/apps-lv`

`sudo mkfs -t ext4 /dev/webdata-vg/logs-lv`

![format](./images/format.PNG)

**followed the following steps**

![sep](./images/sep.PNG)

![cont](./images/cont.PNG)

![cont2](./images/cont2.PNG)

**Updated /etc/fstab file so that the mount configuration will persist after restart of the server**

![fstab](./images/fstab.PNG)

**Test the configuration and reload the daemon with the code below**

`sudo mount -a`

`sudo systemctl daemon-reload`

**verified with dh -h**

![cont3](./images/cont%203.PNG)


## **on my Database server i created volume group, logical volume, formatted my logical volume and then mount it on /db directory i created**

![server1](./images/server%201.PNG)

**also updated my fstab on my database server**

![fstab2](./images/fstab2.PNG)

**verified with dh -h**

![server2](./images/server2.PNG)


**updated both intsances repository with the code below**

`sudo yum -y update`


**followed the steps below**

![step1](./images/step1.PNG)


![cont4](./images/cont%204.PNG)

**continuation**

![step2](./images/step2.PNG)

![cont5](./images/cont5.PNG)

**continuation!!**

![sql client](./images/sql%20client.PNG)

## **finally i used my browser to view my result**

![word 1](./images/word%201.PNG)

![word 2](./images/word%202.PNG)

![word 3](./images/word%203.PNG)

![word 4](./images/word%204.PNG)

![word 5](./images/word%205.PNG)
