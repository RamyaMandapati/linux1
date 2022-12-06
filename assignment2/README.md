# Assignment 2

## Set up the environment:
### 1. Clone the linux repository in to the VM.
### 2. Install the following required packages
        1. sudo apt-get install make
        2. sudo apt install gcc
        3. sudo apt-get install libncurses-dev
        4. sudo apt-get install libssl-dev
        5. sudo apt-get install libelf-dev
 ### 3. Copy the config file " cp /boot/config-5.15.0-1025.gcp .config" 
 ### 4. Remove or comment CONFIG_SYSTEM_TRUSTED_KEYS and CONFIG_SYSTEM_TRUSTED_KEYRING, Change the value of CONFIG_SYSTEM_REVOCATION_KEYS to ""

 ### 5. Run make oldconfig
 ### 6. Build Kernel
          1. make -j 4 modules
          2. make -j 8 (procunits)
          3. sudo make modules_install && sudo make install
          4. sudo reboot
 ### 7. After building the kernel, do changes to cpuid and vmx.c file, and add code to print the data of the leaf nodes.
        Did the code changes for  0xffffffe and oxfffffff
 ### 8. Do the procedure of building the kernel again
 ### 9. After building the kernel successfully, to test the output, we need a nested VM
 ### 10. To install the virtual manager, follow the below steps
          1. Install ubuntu desktop - https://phoenixnap.com/kb/how-to-install-a-gui-on-ubuntu

          2. Install chrome remote desktop - https://ubuntu.com/blog/launch-ubuntu-desktop-on-google-cloud  

          3. Wget https://releases.ubuntu.com/18.04/ubuntu-18.04.6-live-server-amd64.iso to download iso image 

          4. sudo apt-get install virt-manager  - to start virtual manager 
 ### 11. Install the cpuid package
 ### 12. Create a test file and see the output.
 
 
        
