# Slush Pool
The first thing to do is configure your miner. This section covers both Antminer and Whatsminer. 

## Miner configuration
In order to configure your ASIC you will need to be able to communicate with it. The easiest way to do this is to use a web browser to log into your ASIC from a computer connected to the same local network. Once connected and logged into the ASIC you can make the necessary changes to connect to the mining pool. 

First you will need the local IP address for your ASIC. This can be found by logging into your router and checking the list of devices under the DHCP leases section. Your router should have the local IP address needed to login, along with the password on a label somewhere on the device. If not, the directions are usually pretty easy to find with an online search for your manufacturer's router. Typically, you can just type `192.168.0.1` or `192.168.1.1` or `10.0.0.1` into your web browser and that will bring you to your router login page. From there the username/password can vary depending on manufacturer but they are usually something like `admin/admin` or `admin/1234` or `admin/password`. Alternatively, programs like [AngryIP](https://angryip.org/) may be used. 

![](assets/startup0.png)

Once you have your ASIC's local IP address then you can just type that into your web browser URL bar and then you may be warned about how this is not a trusted connection. This is a self signed certificate so just accept the risk and continue. 

<p align="center">
 <img width="450" src="assets/slush9_1.png">
  <img width="450" src="assets/slush10.png">
</p>  

## Antminer
Once you are at the Antminer login page the username/password should be `root/root`.

![](assets/startup1.png)

## Whatsminer
From the Whatsminer login page the username/password should be `admin/admin`.
![](assets/slush11.png)

## Antminer
Once logged in to the Antminer web interface, a few important statistics to note are the Tera Hash, displayed as a Giga Hash Average: `GH/s`. The Fan Speed: `Fan1 Speed`, `Fan2 Speed`, `Fan3 Speed`, `Fan4 Speed`. And the Hash Board Temperatures: `Inlet Temp` & `Outlet Temp`. 

![](assets/startup7_1.png)

## Whatsminer
Once logged in to the Whatsminer web interface, a few important statistics to note are the Tera Hash, displayed as a Giga Hash Average: `GHSav`. The Fan Speed: `FanSpeedIn` & `FanSpeedOut`. The Power Consumption in Watts: `Power`. And the Hash Board Temperatures: `Temperature`. 

![](assets/slush12.png)

It can take several minutes to an hour for the ASIC to get up to speed and fully hashing, in the mean-time you can get started on connecting your ASIC to SlushPool. 

## Connecting to SlushPool
In this section you will see how to connect to SlushPool. There are many mining pools to choose from and the basic concepts covered here should be roughly the same for any pool you choose. 

## Antminer
In the Antminer web interface, navigate to `Settings` in the left-hand menu, this will bring you to the configuration page where you can add the pool URLs. 

![](assets/startup2.png)

## Whatsminer
In the Whatsminer web interface, from the top bar menu, select `Configuration` > `Miner Configuration`. This will bring you to the configuration page where the pool URLs can be added. 

![](assets/slush13.png)

## Antminer
In the Antminer configuration page, you can change all the variables and then click on `Save` at the end prior to reboot. 

![](assets/startup3_1.png)

## Whatsminer
In the Whatsminer configuration page it is important to click on <kbd>Save & Apply</kbd> in between each change you make. Then at the end, after all the changes have been made, the ASIC gets a reboot and the changes are applied. If you don't click <kbd>Save & Apply</kbd> between each change then those changes will be lost prior to the reboot. 

![](assets/slush14.png)

## Antminer & Whatsminer
In another tab on your web browser, log into your SlushPool account if you haven't already. Then navigate to the `Workers` tab in the left-hand side menu and click on `Connect Workers +`.

![](assets/slush15.png)

This will bring up a page where you can choose the SlushPool server that is closest to your geographic location. Choosing a server that is far from you can introduce latency which reduces mining rewards. For the Whatsminers, make sure you have `Stratum V1` selected. Only use `Stratum V2` if you have done the BraiinsOS firmware upgrade on your Antminer. You will also notice that SlushPool suggests that you name your ASIC `username.worker1` in your ASIC configuration page. So in this example, the SlushPool username is `alice123` therefore the ASIC configuration will be setup so that the ASIC is named `alice123.worker1`. If you are running multiple ASICs then just keep appending the "worker" flag sequentially. For example, `alice123.worker1` for the first ASIC. Then `alice123.worker2` in the second ASIC's configuration page, and so on. 

Also of note is that the password in the configuration page can be anything such as `1234`, there is no security precaution with this password, it is used as a way to prevent the mining pool servers from getting spammed. 

![](assets/slush16.png)

## Antminer
Copy/paste the first nearest SlushPool server into your ASIC configuration page by navigating to the `Pool 1` dialog box and placing the SlushPool URL there. 

![](assets/startup3_2.png)

## Whatsminer
Copy/paste the first nearest SlushPool server into your ASIC configuration file by navigating to the `Pool 1` drop down menu and selecting `-- Custom --` and then pasting the SlushPool URL there. Then click on `Save & Apply` before making any other changes. 

<p align="center">
  <img width="798" src="assets/slush17.png">
  </p>

![](assets/slush18.png)

## Antminer
Name your ASIC using your SlushPool username followed by `.worker1` for example, `alice123.worker1`. 

![](assets/startup3_3.png)

## Whatsminer
Name your ASIC using your SlushPool username followed by `.worker1` for example, `alice123.worker1`. Then click on `Save & Apply` before making any other changes. 

![](assets/slush19.png)

## Antminer
You can use any password such as `1234`. Then click on `Save`.

![](assets/startup3_4.png)

## Whatsminer
You can leave the default password as `1234`.

![](assets/slush19_1.png)

## Antminer & Whatsminer
Repeat this process for the other two failover servers, picking a different server for each. Keep the worker name and password the same for each. Make sure you save your setting changes prior to reboot.  

![](assets/startup3_5_1.png)

![](assets/slush19_1.png)

## Antminer
The ASIC needs to be rebooted in order for these changes to take effect. Click on <kbd>Restart Miner</kbd> in the lower right-hand corner, then again in the pop-up prompt. You should hear the fans spool down and back up again.

![](assets/startup4.png)

## Whatsminer
The ASIC needs to be rebooted in order for these changes to take effect. Navigate to `System` > `Reboot` then click on the <kbd>Perform reboot</kbd> button. You will be logged out of the interface and the ASIC will reboot. You will hear the fans spool up and down a couple times. Then you can log back into the ASIC interface. 

<p align="center">
  <img width="733" src="assets/slush20.png">
  </p>
  
![](assets/slush18.png)

## Antminer & Whatsminer
After a few minutes and as long as 90 minutes, you should start to see activity showing up in your SlushPool dashboard. Do not be alarmed if the hash rate is low or if the worker is showing as `Offline` or `Disabled`, it can take a long time for everything to connect and settle down. 

![](assets/slush22.png)

At this point, simply monitor both your SlushPool dashboard and the ASIC web interface to ensure that the amount of hash being generated at the interface is reaching the dashboard. 

![](assets/slush23.png)
![](assets/slush24.png)
![](assets/startup7_1.png)

Keep in mind that the prominently displayed hash rate score on the SlushPool interface is your scoring rate which is made of averages. During initial startup do not be surprised if this number is significantly lower than the hash rate reading you get from the web interface on your ASIC. A more accurate metric to watch is in the upper right-hand corner of your SlushPool dashboard, the `5 minute`, `1 hour`, and `24 hour` averages. 

In the next section on Sparrow Wallet, you will see how to setup a wallet and generate a receiving address. Once you have that address, you can use it to setup your payout rules in your SlushPool dashboard. Navigate to the `Funds` tab in the upper menu bar. 

![](Assets/Slush5.png)

Next, navigate to the row labeled `Bitcoin Account` and on the right-hand side click on the `Set up` hyperlink. Then click on the `Create New Wallet` option. Then fill in a wallet name, your bitcoin deposit address from your preferred wallet, and select a Trigger Type of either `threshold` or `time interval`. With small scale mining operations it may make more sense to use the `threshold` option so that once the accumulated rewards exceed a specified threshold, the payout is made. Specifying a threshold value lower than 0.01 bitcoin will result in a small fee. Then click on `Confirm Changes`.  

![](Assets/Slush6.png)
![](Assets/Slush7.png)

You will be asked to confirm your SlushPool password and you will be sent a confirmation email asking for you to confirm the deposit address change. After clicking on the confirmation link in your email, you will be directed to a new SlushPool window and you will see that your changes have taken effect. 

That is the process for updating your payout address. There are privacy benefits to only using addresses one time, so consider updating this address between each payout. At this point your SlushPool account is all setup and ready to use. If you want additional details for creating a SlushPool account, check the [Upstream Data Startup Guide](https://econoalchemist.github.io/UpstreamData-Startup/04%20Creating%20a%20SlushPool%20Account.html).
