# Ignition autogeneration for Fedora CoreOS

Набор скриптов для автогенерации ignition-конфигов для coreos

В набор входят:
- Настройка для OpenSSH-сервера, авторизация по ключам пользователя github
- Настройка репозиториев K8s

## Что это?

Ignition - формат конфига для настройки Fedora CoreOS во время установки. Подробней - [тут](https://docs.fedoraproject.org/en-US/fedora-coreos/producing-ign/)

## Как использовать:

1. `git clone`
2. `npm run setup` - создаем нужные папки, скачиваем утилиты для работы всех скриптов
3. `npm run preheat` - генерируем ignition для внедряемых конфигов (openssh и k8s)
4. `npm run ignite <host>` - генерируем ignition для хоста
5. (опционально) `npm run serve` - запускаем [веб-сервер](https://github.com/TheWaWaR/simple-http-server), который по сети позволяет использовать конфиги.
