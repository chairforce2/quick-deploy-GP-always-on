# quick-deploy-GP-always-on
Short guide with no explanation of how to deploy my GP always on template on Azure, with certificates, decryption, etc


Step 1:
Deploy this Azure template: https://github.com/wwce/azure-arm/tree/master/Azure-Common-Deployments/v1/1fw_3nic_avset

Step 2: import this named config and commit it (make sure you have and admin un/pwd you know
https://github.com/chairforce2/PANOS-Azure-Config-GP/blob/main/PANOS10-Always-on-VPN-decrypt-template.xml

Step 3: make sure any/all test clients have the root CA from the above template in their trust store so everything works right

Step 4: update GoDaddy domain 

point fwadmin.chairforce2.com to the new fw admin interface IP
point vpn.chairforce2.com to the new untrust interface IP

commit everything and test
