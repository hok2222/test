# Получение сведений о системе
Шаршов Иван

# Получение сведений о системе

## Цель работы

Получить сведения об используемой системе

## Исходные данные

1.  Ноутбук Huawei

2.  Windows

## План

1.  Ввод команд в эмулятор терминала

2.  Анализ данных

## Ход работы

1.  Затем получим сведения о версии ядра:

``` bash
uname -r
```

    5.15.90.1-microsoft-standard-WSL2

1.  Далее можно получить сведения о процессоре:

``` bash
cat /proc/cpuinfo | grep "model name"
```

    model name  : AMD Ryzen 5 5500U with Radeon Graphics
    model name  : AMD Ryzen 5 5500U with Radeon Graphics
    model name  : AMD Ryzen 5 5500U with Radeon Graphics
    model name  : AMD Ryzen 5 5500U with Radeon Graphics
    model name  : AMD Ryzen 5 5500U with Radeon Graphics
    model name  : AMD Ryzen 5 5500U with Radeon Graphics
    model name  : AMD Ryzen 5 5500U with Radeon Graphics
    model name  : AMD Ryzen 5 5500U with Radeon Graphics
    model name  : AMD Ryzen 5 5500U with Radeon Graphics
    model name  : AMD Ryzen 5 5500U with Radeon Graphics
    model name  : AMD Ryzen 5 5500U with Radeon Graphics
    model name  : AMD Ryzen 5 5500U with Radeon Graphics

1.  Далее получим последние 30 строк логов системы:

``` bash
dmesg | tail -n 30
```

    [    3.718927] 9pnet_virtio: no channels available for device drvfs
    [    3.719815] WSL (1) WARNING: mount: waiting for virtio device drvfs
    [    3.771564] hv_pci 5ab84fe2-87a3-4a3d-9a3a-98fd7b0c9fbc: PCI host bridge to bus 87a3:00
    [    3.772576] pci_bus 87a3:00: root bus resource [mem 0xbffe10000-0xbffe12fff window]
    [    3.773563] pci_bus 87a3:00: No busn resource found for root bus, will use [bus 00-ff]
    [    3.775712] pci 87a3:00:00.0: [1af4:1049] type 00 class 0x010000
    [    3.777505] pci 87a3:00:00.0: reg 0x10: [mem 0xbffe10000-0xbffe10fff 64bit]
    [    3.779103] pci 87a3:00:00.0: reg 0x18: [mem 0xbffe11000-0xbffe11fff 64bit]
    [    3.780701] pci 87a3:00:00.0: reg 0x20: [mem 0xbffe12000-0xbffe12fff 64bit]
    [    3.786759] pci_bus 87a3:00: busn_res: [bus 00-ff] end is updated to 00
    [    3.787483] pci 87a3:00:00.0: BAR 0: assigned [mem 0xbffe10000-0xbffe10fff 64bit]
    [    3.789027] pci 87a3:00:00.0: BAR 2: assigned [mem 0xbffe11000-0xbffe11fff 64bit]
    [    3.790656] pci 87a3:00:00.0: BAR 4: assigned [mem 0xbffe12000-0xbffe12fff 64bit]
    [    3.827526] hv_pci 8c620dde-404b-48a4-a7ce-2405c60257ff: PCI VMBus probing: Using version 0x10003
    [    3.883779] hv_pci 8c620dde-404b-48a4-a7ce-2405c60257ff: PCI host bridge to bus 404b:00
    [    3.884781] pci_bus 404b:00: root bus resource [mem 0xbffe14000-0xbffe16fff window]
    [    3.885703] pci_bus 404b:00: No busn resource found for root bus, will use [bus 00-ff]
    [    3.887786] pci 404b:00:00.0: [1af4:1049] type 00 class 0x010000
    [    3.889775] pci 404b:00:00.0: reg 0x10: [mem 0xbffe14000-0xbffe14fff 64bit]
    [    3.891388] pci 404b:00:00.0: reg 0x18: [mem 0xbffe15000-0xbffe15fff 64bit]
    [    3.893058] pci 404b:00:00.0: reg 0x20: [mem 0xbffe16000-0xbffe16fff 64bit]
    [    3.898582] pci_bus 404b:00: busn_res: [bus 00-ff] end is updated to 00
    [    3.899625] pci 404b:00:00.0: BAR 0: assigned [mem 0xbffe14000-0xbffe14fff 64bit]
    [    3.901502] pci 404b:00:00.0: BAR 2: assigned [mem 0xbffe15000-0xbffe15fff 64bit]
    [    3.902672] pci 404b:00:00.0: BAR 4: assigned [mem 0xbffe16000-0xbffe16fff 64bit]
    [    4.078491] misc dxg: dxgk: dxgkio_query_adapter_info: Ioctl failed: -22
    [    4.079453] misc dxg: dxgk: dxgkio_query_adapter_info: Ioctl failed: -22
    [    4.080682] misc dxg: dxgk: dxgkio_query_adapter_info: Ioctl failed: -22
    [    4.081541] misc dxg: dxgk: dxgkio_query_adapter_info: Ioctl failed: -22
    [    4.082363] misc dxg: dxgk: dxgkio_query_adapter_info: Ioctl failed: -2

## Оценка результата

В результате лабораторной работы была получена базовая информация об
используемой системе.

## Вывод

Таким образом. мы научились, используя команды Windows, получать
сведения о системе.
