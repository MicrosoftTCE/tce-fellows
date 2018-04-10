# Intelligent Kiosk Event Setup

Intelligent Kiosk is a Microsoft Azure application built on top of the [Microsoft Cognitive Services APIs](https://www.microsoft.com/cognitive-services). Below are simple setup instructions for configuration:

# Requirements
* A Windows 10 computer (Your Surface Pro should work fine).
* A webcam, ideally top-mounted (TCE-NY owns [this Logitech](http://www.bestbuy.com/site/logitech-hd-webcam-c615-black/2588445.p?skuId=2588445&extStoreId=&ref=212&loc=1&ksid=24143291-22dc-4093-87e2-de89697b7d54&ksprof_id=8&ksaffcode=pg199033&ksdevice=c&lsft=ref:212,loc:2)).
* The [Intelligent Kiosk App](https://www.microsoft.com/en-us/store/p/intelligent-kiosk/9nblggh5qd84).
* Internal S0 (Standard) API Keys (Located in the TCE-NY LastPass account under "Secure Notes"). Keys can also be accessed in the Azure Portal by searching "Cognitive Services". They are listed under the "kiosk-cog-service-keys" resources group and each name begins with "kiosk-".
* A Surface Pro HDMI adapter, if connecting to an external monitor. 

# Setup
See the [Intelligent Kiosk Guide](https://microsoft.sharepoint.com/teams/CECloudML/_layouts/15/WopiFrame.aspx?sourcedoc={DEC7E276-B5B9-45C8-B43C-B5EA651DB134}&file=Face%20API%20Explorer%20Instructions.docx&action=default).

Remember to change your power plan settings to prevent the Surface Pro from going to sleep during demo. See [here](https://www.groovypost.com/howto/microsoft-surface-rt-sleep-power-options/) for instructions.

Source code for the project can be found [here](https://github.com/Microsoft/Cognitive-Samples-IntelligentKiosk).
