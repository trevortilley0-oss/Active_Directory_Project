# Active Directory VMware Project
This project outlines and implements the installation and configuration of Active directory Users, groups, OU's etc.
# Environments and Technologies Used

* VMware

* Active Directory Domain Services

# Operating Systems Used

* Windows Server 2022

* Windows 10 (22H2)

# Deployment and Configuration Steps

### Step 1: Setup Virtual Machines

* Create two virtual machines
  * The first machine will be the domain controller using Windows Server 2022
  * The second machine will be the user logging into the domain using Windows 10
  * Once you load the Windows Server VM you will be loaded straight into the Server manager, but you will notice that active directory is missing this will need to be fixed
    <img width="819" height="580" alt="Missing AD" src="https://github.com/user-attachments/assets/45a880c9-dd2a-4e50-8543-10d9476ed497" />


  * Oh the home page click on add roles and features
  * Accept all the default options untill you get to the server roles step
  * I will be seleceting Active directory and remote access but you are free to choose what you need'
  * Accept all other default options and choose DirectAccess on the role services section
  * Then click install

    <img width="819" height="580" alt="setup" src="https://github.com/user-attachments/assets/e3459521-cee1-4cb3-b02e-395b1e459c3a" />
