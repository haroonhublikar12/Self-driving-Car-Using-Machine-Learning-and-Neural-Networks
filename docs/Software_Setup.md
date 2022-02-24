# Software Setup


After finishing these steps, you'll be all set to program JetRacer.  Once you're finished, run through the [running the software](Running_the_software.md).

## Step 1 - Flash micro SD card

1. Download a JetCard SD card image listed in below table in your laptop/desktop.
2. Insert your micro SD card into the laptop/desktop
3. Format your micro micro SD card using [SD Memory Card Formatter for Windows](https://www.sdcard.org/downloads/formatter/sd-memory-card-formatter-for-windows-download/)
4. Using [Etcher](https://www.balena.io/etcher/) select the downloaded zip file and flash it onto the SD card
5. Remove the SD card from the laptop/desktop
6. If you are confused with how to flash an SD card image [follow this tutorial by NVIDIA](https://developer.nvidia.com/embedded/learn/get-started-jetson-nano-devkit)  (please note: use the below SD card image only...)

### Latest Release 

> Please note, the password for the pre-built SD card is ``jetson``

| Platform | Board revision | JetPack Version | Download | MD5 Checksum |
| -------- | -------------- | --------------- | -------- |------------- |
| Jetson Nano (4GB) | `A02` and `B01` | 4.5.1 |  [jetcard_nano-4gb-jp451.zip](https://drive.google.com/file/d/1aPbzQ0_Uja0jVD48oZUAuYYAz10JgbZu/view?usp=sharing) | 3195c91e6069c0418ec3c9736d130d01 |

 


## Step 2 - Power on and connect over USB

1. Insert the configured SD card into the Jetson Nano module

2. Power on your jetson nano by it to the connecting battery 
3. Now connect your Jetson Nano to your laptop/desktop via micro USB cable

4. Open any web browser in your laptop/desktop, and copy paste this IP address ``192.168.55.1:8888`` in the search bar
5. Sign in using the default password ``jetson``
6. Please note: we will be running jetson nano on head-less mode (meaning you won't need display, keyboard and mouse to program your jetson nano). Also never connect your jetson nano to any display, doing this will require you to go through the above process (Power on and connect over USB) again.  

## Step 2 - Connect JetRacer to WiFi

1. Open a terminal in Jupyter Lab by clicking ``File`` -> ``New`` -> ``Terminal``

2. In the terminal, type the following command to list available WiFi networks, and find the ``ssid_name`` of your network.

    ```bash
    sudo nmcli device wifi list
    ```
3. Connect to  the selected WiFi network

    >  It should be on the same network that you will be webprogramming from

    ```bash
    sudo nmcli device wifi connect <ssid_name> password <password>
    ```
4. Note down the WiFi IP address (``inet``) of the WiFi interface ``wlan0`` returned by the following command.  We'll call this ``jetson_ip_address``
    
    ```bash
    ifconfig
    ```

## Step 4 - Connect to JetRacer over WiFi

1. Unplug the micro USB cable from the Jetson Nano

2. Close the previous Jupyter Lab browser tab
3. Open a new browser tab and navigate to ``http://<jetson_ip_address>:8888``
4. Sign in with the password ``jetson``
    

   
 
## Step 5 - Set the Jetson Nano to 5W mode

To prevent the Jetson Nano from drawing more power than the battery can supply, we set it to 5W mode

1. Open a terminal and call the following to set 5W mode

    ```bash
    sudo nvpmodel -m1
    ```
    
## Next

Next, follow run through the [running the software](Running_the_software.md).
