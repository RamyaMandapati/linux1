## Steps to complete CMPE 283 - Assignment 1 :
* 1. Create GCP account and setup billing.
* 2. Install git and create a repository
* 3. Add Makefile and cmpe-283-1.c files to the repository
* 4. Now, In GCP, go to VM instances under compute engine present in the left menu.
* 5. Create a new VM instance, with the below specifications
       * a. Series : N2
       * b. Machine type : n2-standard
       * c.Boot disk : Operating system : Ubuntu
                      Version : x86/64, amd64 jammy
                      disk : SSD persistent disk
                      size : 100GB
       * d. Allow Firewall 
* 6. Select "Equivalent command line" and copy the code required to create a VM instance from CLI
* 7. Paste this code GCP CLI and add --enable-nested-virtualization --zone=us-central-1a to the code.
* 8. New VM instance will be opened in a new window
* 9. Make necessary changes in the cmpe-283-1.c file to include
*               1. Primary Process based controls (IA32_VMX_PROCBASED_CTLS)
*               2. Secondary process based controls (IA32_VMX_PROCBASED_CTLS2)
*               3. Exit controls (IA32_VMX_EXIT_CTLS)
*               5. Entry controls (IA32_VMX_ENTRY_CTLS)
*               6. Cannot include tertiary controls as it is Can set=No in primary controls
*  10. Now, clone the git repository in the vm instance created in GCP
*  11. Enter into the folder with cd foldername 
*  12. install gcc and make using sudo apt install gcc make
*  13. install sudo apt-get linux-headers-$(uname -r)
*  14. Now, run make command
*  15. If it is successfully executed, cmpe283-1.ko file is generated
*  16. Run command to insert .ko file insmod ./cmpe283-1.ko
*  17. excecute the dmesg command  to view the output as below
*  
<img width="714" alt="Screen Shot 2022-11-04 at 3 26 17 PM" src="https://user-images.githubusercontent.com/101368541/200083900-4e2cbcdc-a0a6-48b5-b2f4-27340a54d333.png">
<img width="714" alt="Screen Shot 2022-11-04 at 3 26 34 PM" src="https://user-images.githubusercontent.com/101368541/200083922-fbe53341-b487-4b87-9443-2f82b28dae85.png">
<img width="681" alt="Screen Shot 2022-11-04 at 3 26 53 PM" src="https://user-images.githubusercontent.com/101368541/200083931-6e474935-28a4-4af3-bcf7-ac1084a339d5.png">
