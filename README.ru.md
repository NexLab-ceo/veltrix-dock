# VELTRIX Dock

**Self-hosted Control Plane и Agent для Android/Termux.**

VELTRIX Dock позволяет управлять сервисами и подключёнными устройствами через веб-панель Control Plane.

## Документация

- **Документация:** https://docs.veltrix.com
- **Загрузки и релизы:** https://github.com/NexLab-ceo/veltrix-dock/releases
- **Исходный код:** https://github.com/NexLab-ceo/veltrix

## Установка

Скачайте подходящий пакет .deb из [последнего релиза](https://github.com/NexLab-ceo/veltrix-dock/releases/latest).

В Termux установите зависимости и выбранный пакет:

    pkg update
    pkg install mariadb php git termux-services
    pkg install ./veltrix-all_<version>_aarch64.deb

Для устройства только с Agent:

    pkg update
    pkg install php git termux-services
    pkg install ./veltrix-agent_<version>_aarch64.deb

Замените <version> на версию из имени скачанного файла. На одном устройстве устанавливайте **один** пакет: veltrix-all для устройства Control Plane (он также содержит Agent) или veltrix-agent для удалённого устройства. Если скачаны оба файла, не используйте маску pkg install ./veltrix-*.deb: она может выбрать оба пакета.

## Пакеты

| Пакет | Содержимое | Назначение |
|---|---|---|
| veltrix-all | Control Plane, Agent, веб-интерфейс, миграции и скрипты установки | Телефон разработчика / главный телефон |
| veltrix-agent | Только Agent и скрипт его настройки | Удалённое устройство |

## Лицензия

VELTRIX Dock — freeware, а не open source. Личное, образовательное и некоммерческое использование бесплатно. Для коммерческого использования требуется отдельная лицензия. См. [LICENSE](LICENSE) и [LICENSE.ru.md](LICENSE.ru.md).

---

© 2026 NexLab. Все права защищены.
