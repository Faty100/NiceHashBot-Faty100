If you have any ideas you want to add let me know ill try to remain active and do my best. Post your ideas here in github. Also my email is fatty_100@outlook.com

I provided the .zip file in the release section both programs are available there. They will be updated once I release the new versions as well.

Donations are welcomed :) Happy Mining

BTC - bc1q09fauqa48utq3wkdyrpvyp223cev558hsppt9c

New Features I am working on

- Adding speed changes based on network difficulty. For example if you are not watching it and network difficuly sky rockets and your using max speed       your chances of getting a block are pretty much none and your contract ends and you get nothing. When the network difficuly changes to a certain number    that you edit your speed will change to the lowest number that you edit as well. Or vice versa either way the goal is to ensure you have control over     what happens to the contract based on network difficulty.


# NiceHashBot - New Features below please read
NHB3 bot for automatic order management.

- [Features](#features)
- [How to run?](#run)
- [How to compile?](#compile)
- [Tips for programmers](#tips)

![](https://raw.githubusercontent.com/nicehash/NiceHashBot/master/screenshots/00nhb3.png)

# <a name="features"></a> Features

New Nicehash bot features

- Added a new option to Auto start the bot when opening the application (I did this because sometimes nicehash bot will crash)
- Added a new program you can download from me called Software Monitor that will check to see if nicehash is running and if its not will load it for you and with Autostart enabled in NHB it will automatically start without you doing anything
- Added a timer edit interval (Right now nicehash has it setup so its every 1 min for the bot to run but with this now you can set it to anytime you want)
- Added a countdown display clock just for visual use
- Added MaxPrice Limit


   Old Features
  
- Run on **test** and **production** environment (instructions on how to obtain API keys https://github.com/nicehash/rest-clients-demo/blob/master/README.md)
- Manage pools (create/edit/delete)
- Manage orders (create/refill/edit/delete)
- Automatically manage orders for **(Bot On mode)**:
    * **price adjustment** - keep price as low as possible (increase and decrease prices)
    * **refilling** - automatically refill order when 90% of available money is consumed
- Console window showing important events, API calls and errors

# <a name="run"></a> Instructions on how to run

- Download binaries from here: https://github.com/nicehash/NiceHashBot/releases
- Extract zip archive
- Run NHB3.exe
- Note: .NET Framework 4.7 or higher is required. You can also run multiple instances of NHB3 - each in own folder with different API credentials.

# <a name="compile"></a> Instructions on how to compile

- Use Visual Studio 2019 or later
- Open project in Visual Studio
- Rebuild & run

# <a name="tips"></a> Tips for programmers

NHB3 is proof of concept (but working) application. It is some how extension of rest-clients-demo (https://github.com/nicehash/rest-clients-demo) and can be used *as is* or upgraded for further improvements in usability and functionality. 
Main purpose is to demonstrate interaction with new NiceHash platform.

NHB3 uses two classes for interaction with NiceHash platform **Api.cs** that prepares all required request headers (authorization - as described here - https://docs.nicehash.com/) and executes remote calls and **ApiConnect.cs** that exposes methods for actions used by NHB3.

Majority of BOT logic is in function **runBot()** inside Home.cs class witch is executed once per minute and then check if order needs some sort of interaction (refill, increase speed or decrease speed).


