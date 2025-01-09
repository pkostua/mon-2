# Решение домашнего задания к занятию 14 «Средство визуализации Grafana»
https://github.com/netology-code/mnt-homeworks/blob/MNT-video/10-monitoring-03-grafana/README.md

## Задание повышенной сложности

1. Compose файл для поднятия стека https://github.com/pkostua/mon-2/blob/master/compose.yml
2. Конфигурация prometheus  https://github.com/pkostua/mon-2/blob/master/prometheus/prometheus.yml
3. Скришот алерта
   ![image](https://github.com/user-attachments/assets/15f379fe-fc5f-4f4c-b844-3f7556fca570)

## Обязательные задания

### Задание 1. Скриншот веб-интерфейса grafana
![image](https://github.com/user-attachments/assets/e0975d18-1e99-460a-b56d-7a4c6bfe2329)

### Задание 2. Скриншот Dashboard
![image](https://github.com/user-attachments/assets/8a33f2dd-822d-46fc-9f18-fbeef7dfb184)

### promsql
```
#утилизация CPU для nodeexporter (в процентах, 100-idle);
100 - avg(irate(node_cpu_seconds_total{mode="idle"}[1m])) * 100

#CPULA 1/5/15;
sum(rate(node_cpu_seconds_total[1m])) by (instance)
sum(rate(node_cpu_seconds_total[5m])) by (instance)
sum(rate(node_cpu_seconds_total[15m])) by (instance)

#количество свободной оперативной памяти;
node_memory_MemAvailable_bytes

#количество места на файловой системе.
node_filesystem_avail_bytes{mountpoint="/"}
```

### Задание 3. Dasboard с настроенными alert
Пришлось изменить тип отображения портомучто для типа Stat алерты недоступны
![image](https://github.com/user-attachments/assets/32949d24-f445-4225-8e18-640abeef71b3)

### Задание 4. Сохраненный Dasboard
https://github.com/pkostua/mon-2/blob/master/dashboard.json
