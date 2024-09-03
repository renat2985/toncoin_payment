
# Оплата ваших услуг через TonCoin

 Удобный и быстрый способ внедрения платных услуг с использованием криптовалюты TonCoin. Процесс простой: Вы открываете любой крипто кошелек, сканируете QR-код, переводите указанную сумму, и как только платеж будет получен, реле активируется и включит ваш прибор на заданное вами время. Это может быть любой прибор, от чайника, кофемашины и лампочки до включения электричества в помещение или любом другом месте.

Вы можете собрать устройство самостоятельно или попросить это сделать меня для вас. Для заказа готового устройства свяжитесь через Telegram или Skype: renat2985.

<img src="https://github.com/renat2985/toncoin_payment/blob/main/doc/1.webp" width="200px" style="float:left">
<img src="https://github.com/renat2985/toncoin_payment/blob/main/doc/2.webp" width="200px" style="float:left">
<img src="https://github.com/renat2985/toncoin_payment/blob/main/doc/3.webp" width="200px" style="float:left">

### Основные функции:

1. **Подключение устройства:**
   - При первом включении или если устройство не может найти роутер, оно создаст точку доступа с именем "TonCoin payment".
     
     <img src="https://github.com/renat2985/toncoin_payment/blob/main/doc/WiFi.png" width="200px">
   - Подключитесь к этой точке (пароль не требуется) и откройте браузер, где введите http://192.168.4.1. Обычно после подключения к Wi-Fi автоматически откроется Activ portal, который перенаправит вас на нужную страницу.
     
     <img src="https://github.com/renat2985/toncoin_payment/blob/main/doc/AP1.png" width="300px">
   - Нажмите "Configure WiFi" для настройки.

2. **Настройка устройства:**
   - **Роутер и пароль:** Введите данные для подключения к вашему Wi-Fi.
   - **Device Name:** Укажите имя устройства, например, "Buy coffee".
   - **Your Toncoin Wallet:** Введите адрес вашего кошелька для приема платежей.
   - **Сurrency:** Выберите валюту, в которой хотите получать оплату (EUR, USD, RUB, BYN, BGN, GBP и др.). Это необходимо для автоматической конвертации суммы в TonCoin на основе текущего курса, который обновляется каждые 3 часа через coinmarketcap.com.
   - **Service Currency Price:** Укажите цену в выбранной валюте, которую клиент должен оплатить. После сканирования QR-кода клиенту будет предложена эквивалентная сумма в TonCoin.
   - **Relay Work Time:** Укажите, на сколько секунд должно включиться реле. Это может быть от одной секунды (например, для имитации нажатия кнопки) до нескольких минут или часов.
     
     <img src="https://github.com/renat2985/toncoin_payment/blob/main/doc/APFull.png" width="500px">





### Инструкции для самостоятельной сборки:

Для самостоятельной сборки устройства вам потребуется устойство smalltv. Обратите внимание есть еще smalltv-ultra и smalltv-pro они внешне одинаковы, но отличаются по внутренней начинке. Проект работает только на smalltv. Дополнительно вам понадобятся:
- Реле-модуль на 5V для Arduino
- Паяльник и провода

На фото ниже показано, как должно быть все припаяно:


  <img src="https://github.com/renat2985/toncoin_payment/blob/main/doc/flash_gpio2.jpeg" width="500px">

Скачайте файл  [toncoin_payment.ino.bin](https://github.com/renat2985/toncoin_payment/raw/main/build/esp8266.esp8266.generic/toncoin_payment.ino.bin) и загрузите его на ноутбук или телефон. Далее с этого устройства подключитель к WiFi гаджета которое будет называться GIFTV далее обязательно открыть браузер и в нем набрать http://192.168.4.1/update
выберите скачанный ранее файл [toncoin_payment.ino.bin](https://github.com/renat2985/toncoin_payment/raw/main/build/esp8266.esp8266.generic/toncoin_payment.ino.bin) и нажмите Upload... 
После этого следуйте инструкциям из пунктов 1 “Подключение устройства” и 2 “Настройки устройства”.

Удачи! Если у вас возникнут вопросы, не стесняйтесь обращаться ко мне.

Важно: Обратите внимание, что каждый 20-й платеж автоматически переводится на мой кошелек TonCoin в качестве небольшого доната за проект. Если вы хотите изменить это и предложить другой способ, пожалуйста, свяжитесь со мной.

# Для совсем профи инструкция для прошивки через программатор

### Specification .bin files
```
  -  Module: Generic ESP8266 Module
  -  Flash Size: 1M
  -  CPU Frequency: 160Mhz
  -  Flash Mode: dio
  -  Flash Frequency: 80Mhz
  -  Upload Speed: 921600
```

## [toncoin_payment.ino.bin](https://github.com/renat2985/toncoin_payment/raw/main/build/esp8266.esp8266.generic/toncoin_payment.ino.bin)

### NodeMCU Flasher
https://github.com/nodemcu/nodemcu-flasher
Download Release: [Win32](https://github.com/nodemcu/nodemcu-flasher/blob/master/Win32/Release/ESP8266Flasher.exe) or [Win64](https://github.com/nodemcu/nodemcu-flasher/blob/master/Win64/Release/ESP8266Flasher.exe).



## :battery: Donation

If you like this project, you can give me a cup of coffee :coffee:

- Bitcoin (BTC): 19xg6pA4RzSW3o4ZUyTyn5t4tY3tqLXHbe
- TonCoin: UQBY_xXK_25L-UHq_h2ocfhS0c_lZoA4PIHxt-SktxLa_So7 
- PayPal [https://www.paypal.me/RKevrels](https://www.paypal.me/RKevrels/5)
