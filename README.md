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

### Step 2: Setup Active Directory
  * On the home page click on add roles and features
   <img width="2506" height="800" alt="68747470733a2f2f692e696d6775722e636f6d2f445152564e6e6d2e706e67" src="https://github.com/user-attachments/assets/591583e4-5501-46b8-9b7f-d098472c148a" />
   
   * Accept all the default options untill you get to the server roles step
   * I will be seleceting Active directory but you are free to choose what you need
   * Accept all other default options
   * Then click install
<img width="738" height="712" alt="68747470733a2f2f692e696d6775722e636f6d2f52707a6e6752692e706e67" src="https://github.com/user-attachments/assets/fa5f242c-c697-4c97-91dc-50fa35d4e62d" />

   * Once that has finished you will need to promote the Server to a Domain Controller

### Step 3: Add the Domain Controller and Forest
   * At the top right of the Server Manager Dashboard, click on the flag
   * Select "Promote This Server to a Domain Controller"
    <img width="3290" height="828" alt="68747470733a2f2f692e696d6775722e636f6d2f474f59695446652e706e67" src="https://github.com/user-attachments/assets/451f8f7a-f51f-4ccf-abed-3446af227f09" />
  * Select "Add a New Forest"
   * Root domain name: (pick domain name).local
   * Once you pick your name you will have to enter ".local" following the name because the server is a local version, otherwise it wont wor
   * Select Next
   * Create a password
   * Select Next and follow the prompts
   * Select Install to complete the installation
    <img width="766" height="555" alt="Screenshot 2026-01-28 180729" src="https://github.com/user-attachments/assets/ccb1b347-0d8e-4d93-86a8-0687246fd304" />

   * The Virtual Machine will restart
   * Log back in with the credentials you created

### Step 4: Create an Admin and Normal User Account in Active Directory
  * Click Tools at the top-right of the screen
  * Select Active Directory Users and Computers
  <img width="792" height="660" alt="68747470733a2f2f692e696d6775722e636f6d2f756447486247732e706e67" src="https://github.com/user-attachments/assets/62c9d313-dac2-4d7d-87f8-5eb4abc38488" />
  
  * Right-click your forest's name (Trevor.local) > New > Select Oranizational Unit (OU)
  * Create two OUs
    * Name the first "Admin"
    * Name the second "Regular User"
   <img width="757" height="528" alt="Screenshot 2026-01-28 183320" src="https://github.com/user-attachments/assets/4e0bc029-b66d-416f-8018-3accf7746d98" />

  * Go to the "Admin" OU
    * Right-click the name of the OU > New > Group
    * Give your group a name
    * Leave all the defaults then press ok
<img width="750" height="571" alt="Screenshot 2026-01-28 184349" src="https://github.com/user-attachments/assets/f516e163-6fd4-4592-a4f8-77081340aceb" />


  * Go to the "Admin" OU
  * Right-click the name of the OU > New > User
    * First/Last name: (Whatever you choose)
    * User login name: (Whatever you choose)
    * Select Next
    * Create a password
    * Uncheck all boxes
    * Select Next and then select Finish
<img width="750" height="571" alt="Screenshot 2026-01-28 184349" src="https://github.com/user-attachments/assets/6cd8fe67-51d7-4942-91b1-0d63ba9d5a70" />
<img width="435" height="376" alt="Screenshot 2026-01-28 183950" src="https://github.com/user-attachments/assets/04a4d31e-d9cb-435c-a024-5ecb3f4b6fba" />

  * Go to the "Admin" OU
  * Right-click Jane Doe > select Properties
    * Click the tab named "Member of" > select Add
    * 

