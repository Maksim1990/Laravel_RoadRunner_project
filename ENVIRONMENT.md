# Доступные переменные окружения

Имя переменной | Значение по-умолчанию | Возможные значения | Описание | Расположение обработчика
:------------: | :-------------------: | :----------------: | -------- | ------------------------
`STARTUP_DELAY` | `0` | `0..999` | Задержка (в секундах) перед запуском процесса в контейнере с приложением | `app-entrypoint.sh`
`STARTUP_WAIT_FOR_SERVICES` | `false` | `true` `false` | Ожидает доступность зависимых сервисов перед запуском процесса в контейнере | `app-entrypoint.sh`
`APP_FORCE_HTTPS` | `false` | `true` `false` | Форсирует работу приложения по протоколу HTTPS (необходимо для формирования корректных ссылок на статику и т.д.) | `app`
`APP_ENV` | `production` | `production` `local` `testing` | Режим работы приложения (особый режим `testing` для unit-тестирования) | `app`
`APP_DEBUG` | `false` | `true` `false` | Режим отладки приложения | `app`
`APP_URL` | `http://localhost` | _Произвольный URI_ | Базовый URI приложения | `app`
`APP_KEY` | `:HIDDEN:` | _Произвольная строка_ | Соль для алгоритмов шифрования данных | `app`
`DB_HOST` | `127.0.0.1` | _IP адрес или имя хоста_ | Хост БД PostgreSQL | `app`
`DB_PORT` | `5432` | _Произвольный номер порта_ | Порт БД PostgreSQL | `app`
`DB_DATABASE` | `processing` | _Произвольное имя БД без пробелов_ | Имя БД в PostgreSQL | `app`
`DB_USERNAME` | `processing` | _Произвольное имя пользователя БД без пробелов_ | Имя пользователя БД PostgreSQL | `app`
`DB_PASSWORD` | `processing` | _Произвольное значение_ | Пароль пользователя БД в PostgreSQL | `app`
`DB_SCHEMA` | `public` | _Произвольное имя схемы_ | Имя схемы БД в PostgreSQL | `app`
`SESSION_DRIVER` | `redis` | `redis` `file` | Драйвер сессий | `app`
`REDIS_HOST` | `127.0.0.1` | _Хост или IP_ | Хост или IP адрес сервера redis | `app`
`REDIS_PASSWORD` | `-` | _Произвольное значение_ | Пароль для доступа к серверу redis | `app`
`REDIS_PORT` | `6379` | _Произвольный номер порта_ | Номер порта для подключению к серверу redis | `app`
`REDIS_DB` | `0` | _Произвольный номер БД redis_ | Номер БД в redis для хранения данных по-умолчанию | `app`
`REDIS_CACHE_DB` | `1` | _Произвольный номер БД redis_ | Номер БД в redis для хранения кэша | `app`
`REDIS_SESSIONS_DB` | `1` | _Произвольный номер БД redis_ | Номер БД в redis для хранения сессий | `app`
`QUEUE_CONNECTION` | `sync` | `redis` `sync` | Имя драйвера очередей | `app`