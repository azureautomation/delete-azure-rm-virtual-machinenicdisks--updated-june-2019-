Delete Azure RM Virtual Machine-NIC-Disks (Updated June 2019)
=============================================================

            

There is a newer version of this script that will delete the VM's in parallel. 


 







Parallel Delete Azure RM Virtual Machine* * 




https://gallery.technet.microsoft.com/scriptcenter/Parallel-Delete-Azure-RM-84dadec9** *** *







 





 


 


This script will delete an Azure Resource manager Virtual Machine.


- It will also delete the associated Network Interface Card (NIC).


- Option to delete Public IP address.


- It will also remove both STANDARD and MANAGED Disks.


   - Including both the OSDisk and the DATADisks.


------------------


This function assumes a few things in relation to the storage of the STANDARD disks, which is that they all use the SAME storage account. 


If your DATA Disks use different storage accounts than your OSDisks, then you need to update the function accordingly.


------------------** *** *


You also need to make sure you are logged into the correct Azure Subscription prior to running this script.


------------------** *** *


The ConfirmImpact is set to high, so by default it will prompt you to confirm the deletion of the virual machine.


E.g.


Remove-AzureRMVMInstanceResource -ResourceGroup AZEUS2-MY-APP  -VMName AZEUS2-DEV03-vmMyApp01


To bypass the prompt use:


E.g.


Remove-AzureRMVMInstanceResource -ResourceGroup AZEUS2-MY-APP  -VMName AZEUS2-DEV03-vmMyApp01 -Confirm:$False


 







Here is another script used to Create a VM 




[https://gallery.technet.microsoft.com/scriptcenter/Deploy-a-new-Virtual-75cd3230](https://gallery.technet.microsoft.com/scriptcenter/Deploy-a-new-Virtual-75cd3230)










 

 

        
    
TechNet gallery is retiring! This script was migrated from TechNet script center to GitHub by Microsoft Azure Automation product group. All the Script Center fields like Rating, RatingCount and DownloadCount have been carried over to Github as-is for the migrated scripts only. Note : The Script Center fields will not be applicable for the new repositories created in Github & hence those fields will not show up for new Github repositories.
