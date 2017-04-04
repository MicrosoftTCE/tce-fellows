
## Tutorial: Setting Up A Virtual Machine on Azure
The tutorial on Microsoft Docs is pretty solid. Tutorial here: <https://docs.microsoft.com/en-us/azure/virtual-machines/windows/quick-create-portal>

### Why?
Because certain Azure desktop apps that cannot be run on Macs i.e. the all-important [PowerBI]. **If you are already using a computer running Windows and/or you would prefer to use your Surface, you won't need to set up a virtual machine (VM).** 

### Prerequisites:
This tutorial assumes you have successfully set up an Azure subscription. If you don't have an Azure subscription, create a [free account] before you begin.

### Notes:
* When choosing the size of your VM (in step 4), choose the cheapest option. You should have been given credits that should cover this cost.

* In 'Open port 80 for web traffic' in Step 1, you can also access the NSG by the following:

Click the **virtual machine icon** that should be on the left (I believe this is what the tutorial refers to as the 'blade'). Then click **the name of your new VM**:
![VM Blade][VMblade]

Click **Network Interfaces**. Then, under Security Group, click the name that **ends with -nsg**:
![nsg][nsg]


[PowerBI]: https://powerbi.microsoft.com/en-us/downloads/
[free account]: https://azure.microsoft.com/en-us/free/

[VMblade]: https://github.com/microsoftny/tce-fellows/blob/master/images/VMblade.jpg?raw=true

[nsg]: https://github.com/microsoftny/tce-fellows/blob/master/images/nsg.jpg?raw=true