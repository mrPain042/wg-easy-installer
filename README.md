
# WG Easy Installer

Скрипт для быстрой и автоматизированной установки панели [WG Easy](https://github.com/WeeJeWel/wg-easy) на сервер Ubuntu.

## Быстрая установка

Чтобы быстро установить WG Easy, выполните следующую команду в терминале вашего сервера Ubuntu:

```bash
bash <(curl -sSL https://raw.githubusercontent.com/mrPain042/wg-easy-installer/main/install_wg_easy.sh)
```

### Этот скрипт выполняет следующие действия:

Обновление пакетов: запускает apt update и apt upgrade, чтобы убедиться, что все пакеты системы актуальны.

Установка Docker: если Docker не установлен, скрипт автоматически устанавливает его с помощью apt install docker.io.
Настройка Docker: запускает и включает Docker, чтобы он автоматически стартовал при загрузке системы.

Генерация пароля и bcrypt-хеша: скрипт создает случайный пароль и его bcrypt-хеш для обеспечения безопасности административной панели.

Получение IP-адреса: автоматически получает публичный IP-адрес сервера для настройки WG Easy.

Запуск WG Easy в Docker: запускает WG Easy в контейнере Docker, используя параметры,
такие как сгенерированный хеш пароля, IP-адрес сервера и порты 51820/UDP и 51821/TCP для доступа к панели.

Вывод информации: после установки скрипт выводит URL для доступа к административной панели и сгенерированный пароль.
Пример вывода после установки

После успешного выполнения скрипта вы увидите сообщение, подобное следующему:

```bash
Установка завершена!
Вы можете получить доступ к панели WG Easy по адресу:
wg-interface: http://ваш_IP_адрес:51821
Пароль администратора: сгенерированный_пароль
```

Этот скрипт предназначен для работы на свежих установках Ubuntu, поэтому включены команды для обновления системы и установки Docker.

Скрипт протестирован на Ubuntu 22.04.
