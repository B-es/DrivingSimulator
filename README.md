# DrivingSimulator

Симулятор дорожного трафика с 3D-визуализацией в реальном времени. Unity отображает трафик, которым управляет SUMO — симулятор городской мобильности.

Основан на репозитории [Real-time Traffic Simulation with 3D Visualisation](https://github.com/DarraghMac97/Real-time-Traffic-Simulation-with-3D-Visualisation).

## Требования

- Unity **2018.2.17**
- SUMO **1.01**

## Структура проекта

```
DrivingSimulator/
├── Sumo Unity/       # Unity-проект (3D-визуализация)
├── SumoSimulation/   # Конфигурация сети SUMO (карта, маршруты)
└── OtherAssets/
```

## Запуск

1. Открыть папку `Sumo Unity` в Unity 2018.2.17 и запустить сцену.
2. В отдельном терминале перейти в папку `SumoSimulation` и выполнить:

```bash
sumo-gui -c map.sumocfg --start --remote-port 4001 --step-length 0.02
```

Unity и SUMO соединятся через порт `4001` по протоколу TraCI.
