# Speedtest
#### Даний модуль вимірює швидкість інтернету
#### Опис

В папці **speedtest_api** знаходиться API для модуля.

##### speedtest_api:
- garbage.cgi - файл для тесту завантаження.
- empty.cgi - файл для тесту відвантаження та пінгу.
- get_ip.cgi - файл для отримання IP.
- speedtest_worker.js - файл з інтерфейсом.

#### Установка:
Каталог модуля перемістити в /usr/abills/Abills/modules/

В терміналі ввести ```sudo ln -s /usr/abills/Abills/modules/Speedtest/speedtest_api /usr/abills/cgi-bin/```, 
```sudo apt install libssl-dev``` та ``` cpan install Crypt::OpenSSL::Random ```.


В файлі **config.pl**:
```
@MODULES = (
             'Speedtest'
           );
```

Для роботи з модулем потрібно виконати установку яка наведена вище. Після установки в кабінеті користувача відобразиться вкладка "Тест швидкості". При натисненні на дану вкладку відобразиться інтерфейс модуля. Для початку тесту потрібно натиснути на кнопку "Почати". Швидкість Download та Upload відображається в Мегабіт/секунду, а швидкість Ping та Jitter в мілісекундах. 

