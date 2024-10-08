# Оплата ваших услуг через TonCoin

 Удобный и быстрый способ внедрения платных услуг с использованием криптовалюты TonCoin. Процесс простой: Вы открываете любой крипто кошелек, сканируете QR-код, переводите указанную сумму, и как только платеж будет получен, реле активируется и включит ваш прибор на заданное вами время. Это может быть любой прибор, от чайника, кофемашины и лампочки до включения электричества в помещение или любом другом месте.

Вы можете собрать устройство самостоятельно или попросить это сделать для вас. Для заказа готового устройства свяжитесь через [Telegram](https://t.me/ESPiotDevice), [Skype](https://skype:renat2985?chat), [Discord](https://discord.com/invite/zaGaDuGe).
У нас есть похожий проект на базе [Sonoff](https://github.com/renat2985/toncoin_payment_sonoff), [ESP32 C3 MINI 1.69inch LCD](https://github.com/renat2985/crypto_payment_touchScreen).

[![IMAGE ALT TEXT HERE](https://github.com/renat2985/toncoin_payment/blob/main/doc/intro4.png)](https://www.youtube.com/watch?v=zKdVJmzJNLM&list=PL6NJTNxbvy-LpsI6D_1RM6v5YWDvsm5j4)


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
   - **CoinMarketCap API:** Это сервис, который позволяет получать текущую цену TonCoin в фиатной валюте. Для тестирования можно не менять API, но если вы планируете использовать устройство на постоянной основе, настоятельно рекомендуется зарегистрироваться на сайте [CoinMarketCap](https://coinmarketcap.com/api/) и получить свой собственный API. Т.к. бесплатная версия позволяет делать до 10 000 запросов в месяц на получение цены. Для 10 устройств этого вполне достаточно, но если наше API будет использоваться большим количеством устройств, не все смогут получать актуальную цену, и в результате оплата может не пройти.
   - **Сurrency:** Выберите валюту, в которой хотите получать оплату (EUR, USD, RUB, BYN, BGN, GBP и др.). Это необходимо для автоматической конвертации суммы в TonCoin на основе текущего курса, который обновляется каждые 3 часа через coinmarketcap.com.
   - **Service Currency Price:** Укажите цену в выбранной валюте, которую клиент должен оплатить. После сканирования QR-кода клиенту будет предложена эквивалентная сумма в TonCoin.
   - **Payment Tolerance:** В этой ячейке указывается допустимая погрешность в цене. Поскольку стоимость Ton подвержена колебаниям, здесь нужно указать допустимое отклонение (в виде одной цифры), которое вы готовы принять при оплате. Это нужно для случаев, когда человек не будет сканировать QR-код, а попытается отправить указанную сумму вручную в фиатной валюте.
   - **Relay Work Time:** Укажите, на сколько секунд должно включиться реле. Это может быть от одной секунды (например, для имитации нажатия кнопки) до нескольких минут или часов.
     
     <img src="https://github.com/renat2985/toncoin_payment/blob/main/doc/APFull.png" width="500px">





### Инструкции для самостоятельной сборки:

Для самостоятельной сборки устройства вам потребуется устойство smalltv или smalltv-ultra. Обратите внимание есть еще smalltv-pro они внешне одинаковы, но отличаются по внутренней начинке. Проект работает только на smalltv, smalltv-ultra. Дополнительно вам понадобятся:
- Реле-модуль на 5V и ULN2003(смотри фото) или 5V Relay Arduino module
- Паяльник и провода

На фото ниже показано, как должно быть все припаяно:

<img src="https://github.com/renat2985/toncoin_payment/blob/main/doc/connect.png" width="300px">
<img src="https://github.com/renat2985/toncoin_payment/blob/main/doc/connect2.png" width="300px">
<img src="https://github.com/renat2985/toncoin_payment/blob/main/doc/soldering.jpg" width="300px">

Скачайте файл  [toncoin_payment.ino.bin](https://github.com/renat2985/toncoin_payment/raw/main/build/esp8266.esp8266.generic/toncoin_payment.ino.bin) и загрузите его на ноутбук или телефон. Далее с этого устройства подключитель к WiFi гаджета которое будет называться GIFTV далее обязательно открыть браузер и в нем набрать http://192.168.4.1/update
выберите скачанный ранее файл [toncoin_payment.ino.bin](https://github.com/renat2985/toncoin_payment/raw/main/build/esp8266.esp8266.generic/toncoin_payment.ino.bin) и нажмите Upload... 

  <img src="https://github.com/renat2985/toncoin_payment/blob/main/doc/flashing.png" width="500px">

После этого следуйте инструкциям из пунктов 1 “Подключение устройства” и 2 “Настройки устройства”.

Удачи! Если у вас возникнут вопросы, не стесняйтесь обращаться ко мне.

# Для совсем профи инструкция для прошивки через программатор

## Web installer (recommended)

## Go to the web installer and follow instructions.

## [https://renat2985.github.io/toncoin_payment/](https://renat2985.github.io/toncoin_payment/)


Specification of [toncoin_payment.ino.bin](https://github.com/renat2985/toncoin_payment/raw/main/build/esp8266.esp8266.generic/toncoin_payment.ino.bin) file
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

If you like this project, you can give me a cup of coffee :coffee:

<img src="https://github.com/renat2985/toncoin_payment/blob/main/doc/donate.png" width="700px">

- PayPal [https://www.paypal.me/RKevrels](https://www.paypal.me/RKevrels/5)