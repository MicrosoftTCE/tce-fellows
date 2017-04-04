
## Tutorial: Setting Up A Virtual Machine on Azure
The tutorial on Microsoft Docs is pretty solid. Tutorial here: <https://docs.microsoft.com/en-us/azure/virtual-machines/windows/quick-create-portal>

### Why?
Because some Azure desktop apps cannot be run on Macs i.e. the all-important [PowerBI]. **If you are already using a computer running Windows or you would prefer to use your Surface, you don't need to set up a virtual machine (VM).** 

### Prerequisites:
This tutorial assumes you have successfully set up an Azure subscription. If you don't have an Azure subscription, create a [free account] before you begin.

### Notes:
* When choosing the size of your VM (in step 4), choose the cheapest option. You should have been given credits that should cover this cost.

* The section 'Open port 80 for web traffic' took me a while to figure out, so here are some clarifying images:

* Click the **virtual machine icon** that should be on the left (I believe this is what the tutorial refers to as the 'blade'). Then click **myVM** (or whatever you named your new VM): 
![VM Blade][VMblade]

* Click **Network Interfaces**. Then, under Security Group, click the name that **ends with -nsg**:
![nsg][nsg]

* ... then continue on with the tutorial.

### End Result
HUZZAH! If you did everything successfully, you should now see your Mac running Windows.  
![Windows on a Mac say whaat][macwin]


[PowerBI]: https://powerbi.microsoft.com/en-us/downloads/
[free account]: https://azure.microsoft.com/en-us/free/

[VMblade]: https://github.com/microsoftny/tce-fellows/blob/master/images/VMblade.jpg?raw=true
[nsg]: https://github.com/microsoftny/tce-fellows/blob/master/images/nsg.jpg?raw=true
[macwin]: https://github.com/microsoftny/tce-fellows/blob/master/images/macwin.jpg?raw=true
"Windows on a Mac say whaat"