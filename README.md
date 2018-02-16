# Deploy a VYOS 1.1.8 Appliance in Fujitsu Cloud Service K5
VYOS 1.1.8 image pre-wrapped for use/import into Fujitsu Cloud Service K5 IaaS

## Image Import Process - Using Fujitsu K5 IaaS Portal
 - Log into the Fujitsu K5 IaaS Portal, navigate to storage -> object storage and create a new container to hold the vyos vmdk image
 - Upload the included vyos_1.1.8.vmdk image into the container created above 
![image](https://user-images.githubusercontent.com/9472095/36319170-f9d3bb68-1339-11e8-8666-451e6dd18d1b.png)

 - Now select Import/Export -> VMImport, and select the container where the image has just been uploaded and complete the remaining fields
 ![image](https://user-images.githubusercontent.com/9472095/36319429-d3067934-133a-11e8-9f08-4847d47ebd37.png)

- After 20 minutes (mileage may vary) you should see something like this
![image](https://user-images.githubusercontent.com/9472095/36319260-46e6f690-133a-11e8-8a4e-45c1c5d51edf.png)

## Image Deployment
This is the same as any other image now on K5. As the VYOS is an appliance with typically at least 2 network interfaces I've included an OpenStack HEAT template in this repo that will deliver the following demonstration architecture for quick and easy testing

![image](https://user-images.githubusercontent.com/9472095/36318162-ebe4e5d4-1336-11e8-9acb-e49470fe211d.png)

### CAUTION: Please don't forget to configure __allowed_address_pairs__ once the network design is complete
See https://docs.openstack.org/dragonflow/latest/specs/allowed_address_pairs.html
