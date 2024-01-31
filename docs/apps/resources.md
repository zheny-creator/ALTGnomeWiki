# Ресурсы

Resources - это простой, но мощный монитор ваших системных ресурсов и процессов, написанный на Rust и использующий GTK 4 и libadwaita в качестве графического интерфейса. Он способен отображать использование и подробную информацию о вашем процессоре, памяти, графических процессорах, сетевых интерфейсах и блочных устройствах. Отображает список запущенных графических приложений и процессов.

## Установка из репозитория

**Resources** можно установить любым привычным и удобным способом

**Установка через терминал**
::: code-group

```shell[apt-get]
su -
apt-get update
apt-get install resources
```
```shell[epm]
epm -i resources
```
:::

## Установка c помощью Flatpak

При наличии пакета [Flatpak](/flatpak), можно установить **Resources** одной командой:

```shell
flatpak flatpak install flathub net.nokyan.Resources
```

## Решение проблемы с неработающим мониторингом карт NVIDIA

При использовании графических карт NVIDIA мониторинг ГП в приложении, установленном из репозитория, может не работать.

Решение:

::: code-group

```shell[apt-get]
su -
apt-get update
apt-get install libnvidia-ml
ln -s libnvidia-ml.so.1 /usr/lib64/libnvidia-ml.so
```
```shell[epm]
epm -i libnvidia-ml
ln -s libnvidia-ml.so.1 /usr/lib64/libnvidia-ml.so
```
:::

Перезагружаем приложение и наслаждаемся!