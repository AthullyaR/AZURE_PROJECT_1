# AZURE_PROJECT_1
# A subnet for firewall and subnet for web app where virtual machine is created (private) and an nginx application is installed. Since it is private only specified user has access to it.
# Request from user goes through firewall and reaches the web app. 
1.Create resource group
2.Create virtual network
  1.Enable bastion
  2.Enable firewall
  3.Create firewall policy
  ![image](https://github.com/AthullyaR/AZURE_PROJECT_1/assets/78737460/16f1bc52-e9b8-404e-a1a0-51bc45ce1bdd)
  ![image](https://github.com/AthullyaR/AZURE_PROJECT_1/assets/78737460/0b8d2ebe-a402-490b-ac3c-9404145ebb91)
3.Create virtual machine
  1.Keep public IP as None under networking
  2.Check the box for deleting NIC when VM is deleted
4.Connect VM to bastion
![image](https://github.com/AthullyaR/AZURE_PROJECT_1/assets/78737460/00a2550c-e84d-43d7-8892-fbe276c2ba96)
5.Go to firewall policies
  1.Add DNAT rules
  ![image](https://github.com/AthullyaR/AZURE_PROJECT_1/assets/78737460/53e9d227-9352-41ac-bef0-d1d1366091f5)
  ![image](https://github.com/AthullyaR/AZURE_PROJECT_1/assets/78737460/1e048987-0d99-4a07-a84d-75df566d79a2)
  source ip=user ip
  Destination ip=firewall ip
  Translated ip=VM ip
  6.firewall ip:4000, you will get access to the html content in VM
![image](https://github.com/AthullyaR/AZURE_PROJECT_1/assets/78737460/24bd88ed-784f-494c-909c-2c02f0a2a04c)






