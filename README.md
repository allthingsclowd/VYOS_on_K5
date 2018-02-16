# Deploy a VYOS 1.1.8 Appliance in Fujitsu Clous Service K5
VYOS 1.1.8 image pre-wrapped for use/import into Fujitsu Cloud Service K5 IaaS

# Image Import Process - Using Fujitsu K5 IaaS Portal
 - Log into the Fujitsu K5 IaaS Portal, navigate to storage -> object storage and create a new container to hold the vyos vmdk image
 - Upload the included vyos_1.1.8.vmdk image into the container created above 
![image](https://user-images.githubusercontent.com/9472095/36319170-f9d3bb68-1339-11e8-8666-451e6dd18d1b.png)

 - Now select Import/Export -> VMImport, and select the container where the image has just been uploaded
 
 

![image](https://user-images.githubusercontent.com/9472095/36319260-46e6f690-133a-11e8-8a4e-45c1c5d51edf.png)
