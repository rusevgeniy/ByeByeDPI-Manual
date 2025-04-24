> [!WARNING]
> Гораздо проще использовать и настраивать [ByeDPI manager](https://github.com/romanvht/ByeDPIManager) - он помогает управлять ByeDPI. В случае ручной установки роль менеджера будет на вас.

У вас уже есть ByeByeDPI на вашем Android-устройстве. Вы подобрали работающую стратегию, и у вас заработал YouTube.
Переходим по [ссылке](https://github.com/spvkgn/byedpi), ищем на странице **Releases**  и переходим. Качаем byedpi-16-x86_64-w64.zip.

В корне диска C:\ создаём папку с названием byedpi, из скаченного архива извлекаем в эту папку файлы.

Файл service_install правой кнопкой мыши (далее читать как пкм), изменить в блокноте.

Строку которая начинается на `set svc_bin="\"%cd%\ciadpi.exe\"` меняем: удаляем символы внутри  кавычек, и вместо них вписываем ту стратегию, которая работает на вашем Android-устройстве. Должно получиться примерно так:

<img src="images/Pasted image 20250321232408.png" width="700">

Далее в блокноте файл -> сохранить.

service_install пкм -> запуск от имени администратора, подробнее, выполнить в любом случае, Да.
Выйдет окно терминала, нажать на пробел. В конце должно выйти так, и окно исчезнет после нажатия пробела.


<img src="images/Pasted image 20250321232617.png" width="700">

Можно использовать [Proxy SwitchyOmega 3](https://chromewebstore.google.com/detail/proxy-switchyomega-3-zero/pfnededegaaopdmhkdmcofjmoldfiped?hl=ru&utm_source=ext_sidebar) или [FoxyProxy](https://chromewebstore.google.com/detail/foxyproxy/gcknhkkoolaabfmlnjonogaaifnjlfnp?hl=ru&utm_source=ext_sidebar) для Chromium-подобных браузеров. Или [ZeroOmega--Proxy SwitchyOmega V3](https://addons.mozilla.org/ru/firefox/addon/zeroomega/?utm_source=addons.mozilla.org&utm_medium=referral&utm_content=search) для Firefox.
Настройка идентична [настройке](features.md#расширение-для-браузера) на телефоне.

C сайта браузера [Mozilla Firefox](https://www.mozilla.org/ru/firefox/download/thanks/) качаем и  устанавливаем его.
Открываем , настройки, опускаемся в самый низ, Настройка сети, Настроить.

<img src="images/Pasted image 20250321233320.png" width="700">

Жмём ок, и всё работает.

> [!TIP]
> Желательно использоваться стратегии которые работают с UDP , в противном случае в браузере, понадобится отключать QUIC. 

Инструкцию подготовил **karlosu**
