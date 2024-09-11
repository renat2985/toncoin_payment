[🇷🇺 Русская версия документации здесь](https://github.com/renat2985/toncoin_payment/blob/main/README_RU.md)

# Payment for Your Services via TonCoin

A convenient and fast way to implement paid services using the TonCoin cryptocurrency. The process is simple: You open any crypto wallet, scan the QR code, transfer the specified amount, and once the payment is received, the relay is activated and turns on your device for the time you set. This can be any device, from a kettle, coffee machine, and light bulb to powering a room or any other location.

You can assemble the device yourself or ask to do it for you. To order a ready-made device, contact me via [Telegram](https://t.me/ESPiotDevice), [Skype](https://skype:renat2985?chat), [Discord](https://discord.com/invite/zaGaDuGe).

<img src="https://github.com/renat2985/toncoin_payment/blob/main/doc/intro3.png">

### Main Features:

1. **Connecting the Device:**
   - On the first power-up or if the device cannot find the router, it will create an access point named "TonCoin payment."
     
     <img src="https://github.com/renat2985/toncoin_payment/blob/main/doc/WiFi.png" width="200px">
   - Connect to this access point (no password required) and open a browser, where you enter http://192.168.4.1. Typically, after connecting to Wi-Fi, the Captive Portal will automatically open and redirect you to the required page.
     
     <img src="https://github.com/renat2985/toncoin_payment/blob/main/doc/AP1.png" width="300px">
   - Click "Configure WiFi" to configure the settings.

2. **Configuring the Device:**
   - **Router and Password:** Enter the details to connect to your Wi-Fi.
   - **Device Name:** Specify the name of the device, for example, "Buy coffee."
   - **Your Toncoin Wallet:** Enter your wallet address to receive payments.
   - **Currency:** Choose the currency in which you want to receive payments (EUR, USD, RUB, BYN, BGN, GBP, etc.). This is necessary for automatic conversion of the amount into TonCoin based on the current exchange rate, which is updated every 3 hours via coinmarketcap.com.
   - **Service Currency Price:** Specify the price in the selected currency that the client needs to pay. After scanning the QR code, the client will be prompted with the equivalent amount in TonCoin.
   - **Relay Work Time:** Specify how long the relay should be activated. This can be from one second (e.g., to simulate a button press) to several minutes or hours.
     
     <img src="https://github.com/renat2985/toncoin_payment/blob/main/doc/APFull.png" width="500px">

### Instructions for DIY Assembly:

For DIY assembly, you will need a smalltv or smalltv-ultra device. Note that there are also smalltv-pro, which look the same but differ internally. The project only works on smalltv, smalltv-ultra. Additionally, you will need:
- 5V Relay Module and ULN2003(look photo) or 5V Relay Arduino module
- Soldering iron and wires

The image below shows how everything should be soldered:

  <img src="https://github.com/renat2985/toncoin_payment/blob/main/doc/soldering.jpg" width="300px">

Download the file [toncoin_payment.ino.bin](https://github.com/renat2985/toncoin_payment/raw/main/build/esp8266.esp8266.generic/toncoin_payment.ino.bin) and upload it to your laptop or phone. Then, connect to the WiFi of the gadget, which will be named GIFTV. Next, open a browser and go to http://192.168.4.1/update, select the previously downloaded file [toncoin_payment.ino.bin](https://github.com/renat2985/toncoin_payment/raw/main/build/esp8266.esp8266.generic/toncoin_payment.ino.bin), and click Upload... 

  <img src="https://github.com/renat2985/toncoin_payment/blob/main/doc/flashing.png" width="500px">

After this, follow the instructions from steps 1 “Connecting the Device” and 2 “Configuring the Device.”

Good luck! If you have any questions, feel free to contact me.

Important: Please note that every 30th payment is automatically transferred to my TonCoin wallet as a small donation for the project. If you wish to change this or propose another method, please contact me.

# For Advanced Users: Instructions for Flashing via Programmer

### Web installer (recommended)

Go to the web installer and follow instructions.

[https://renat2985.github.io/toncoin_payment/](https://renat2985.github.io/toncoin_payment/)


### Specification of [ESP8266.bin](https://github.com/renat2985/toncoin_payment/raw/main/build/esp8266.esp8266.generic/toncoin_payment.ino.bin) / [ESP8285.bin](https://github.com/renat2985/toncoin_payment/raw/main/build/esp8266.esp8266.esp8285/toncoin_payment.ino.bin) Files
```
  -  Module: Generic ESP8266 Module
  -  Flash Size: 4M
  -  CPU Frequency: 80Mhz
  -  Flash Mode: DOUT
  -  Flash Frequency: 40Mhz
  -  Upload Speed: 921600
```

### NodeMCU Flasher
https://github.com/nodemcu/nodemcu-flasher
Download Release: [Win32](https://github.com/nodemcu/nodemcu-flasher/blob/master/Win32/Release/ESP8266Flasher.exe) or [Win64](https://github.com/nodemcu/nodemcu-flasher/blob/master/Win64/Release/ESP8266Flasher.exe).

## :battery: Donation

If you like this project, you can buy me a cup of coffee :coffee:

<img src="https://github.com/renat2985/toncoin_payment/blob/main/doc/donate.png" width="700px">

- PayPal [https://www.paypal.me/RKevrels](https://www.paypal.me/RKevrels/5)