# Setup
## Конфигуратор

[Конфигуратор](https://teamgloomy.github.io/Configurator/)

## Структура папок на флешке

[SD_card_structure](https://duet3d.dozuki.com/Wiki/Firmware_Overview#Section_SD_card_structure)
### /gcodes

- для хранения файлов g-кода для печати.
- возможны подпапки.
- G-код может быть на внешней SD-карте

###  /sys

#### sys/board.txt
```
board = fly_E3;

// Smart Drivers
stepper.numSmartDrivers 	= 4;
stepper.TmcDiagPins 		= { A.2, A.1, C.5};

// ESP Settings
8266wifi.espDataReadyPin 	= E.13;
8266wifi.TfrReadyPin 		= E.14;
8266wifi.espResetPin 		= E.15;
8266wifi.serialRxTxPins 	= { D.9, D.8 };

// termistor
heat.tempSensePins 			= { A.3 , A.4 };

```
#### sys/config.g
Плата Fly-E3 поставляется без прошивки на чипе Wi-Fi.

Откройте файл config.g, который был помещен в папку sys на SD-карте, и закомментируйте любые команды M552, которые там используются; например ; M552 S1.

```
M552 S1 ; соединение Wi-Fi при запуске

```

#### sys/homex.g
```
```

#### sys/homey.g
```
```

#### sys/homez.g
```
```
I still don’t have a workout sensorless.
if you measure the voltage, when the motor stops, should it become a logical 0?
