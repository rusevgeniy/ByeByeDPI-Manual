# Другое

1. [Клиенты YouTube](#клиенты)
2. [Про DNS](#dns)
3. [Другие варианты ускорения серверов](#other-options)
     - [На Android](#other-android)
     - [На Windows](#other-windows)
     - [На Linux](#other-linux)
     - [На роутере](#other-router)
     - [На домашнем сервере (постоянно включенном устройстве)](#other-home-server)
     - [На Mac](#other-mac)
4. ["Стандартный редактор" - нужен ли?](#ui-editor)
5. [Универсальная стратегия](#universal)

## <a id="клиенты">Клиенты YouTube</a>

Если вас по каким-то причинам не устраивает оригинальное приложение YouTube, вот несколько альтернативных:

#### Для телевизоров и приставок

- [YouTube for Androuid TV](https://play.google.com/store/apps/details?id=com.google.android.youtube.tv) - официальное приложение YouTube для управления пультом. Требуется Android 7.0+
- [SmartTube](https://github.com/yuliskov/SmartTube) - единственный клиент с поддержкой прокси. Требуется Android 4.3+

#### YouTube с патчами

- YouTube ReVanced. [Revanced Manager](https://revanced.net/revanced-manager) - приложение для удобного скачивания и обновления ReVanced и MicroG. [revanced.app](https://revanced.app/) - Официальный сайт ReVanced. Требуется Android 8.0+
- YouTube ReVanced Extended - если у вас проблемы с QUIC. Требуется Android 8.0+

##### Для продвинутых

> [!TIP]
> Для установки YouTube ReVanced и YouTube ReVanced Extended рекомендуется патчить приложение самостоятельно:

- [YouTube ReVanced Manager](https://github.com/ReVanced/revanced-manager)
- [RVX Manager](https://github.com/inotia00/revanced-manager)

#### NewPipe и его вариации

- [NewPipe](https://github.com/TeamNewPipe/NewPipe/releases) -  клиент для YouTube, который не использует каких-либо библиотек, зависящих от Google. Отсутствует функция авторизации в google аккаунт. Требуется Android 5.0+
- [BravePipe](https://github.com/bravenewpipe/NewPipe) - форк NewPipe с поддержкой Sponsorblock, улучшенными фильтрами поиска и сортировки. Есть импорт подписок с помощью Google Takeout. Требуется Android 4.4+ (не проверено)
- [PipePipe](https://github.com/InfinityLoop1308/PipePipe) - форк NewPipe с большим количеством сервисов, клиентских функций и исправлений ошибок. Требуется Android 5.0+
- [Tubular](https://github.com/polymorphicshade/Tubular) - форк NewPipe c поддержкой Sponsorblock и ReturnYouTubeDislike. Требуется Android 5.0+

#### SkyTube

- [SkyTube Extra](https://github.com/SkyTubeTeam/SkyTube) - простой и функциональный проигрыватель видео с YouTube. Поддерживает официальный плеер и Chromecast. Требуется Android 4.4+
- [SkyTube](https://github.com/SkyTubeTeam/SkyTube) - простое и функциональное свободное приложение для проигрывания видеороликов с YouTube, которое не требует Google Play Services для работы. Требуется Android 4.4+
- [SkyTube Legacy Extra](https://github.com/SkyTubeTeam/SkyTubeLegacy) - простой и функциональный проигрыватель видео с YouTube. Поддерживает официальный плеер и Chromecast. Требуется Android 4.0+
- [SkyTube Legacy](https://github.com/SkyTubeTeam/SkyTubeLegacy) - простое и функциональное свободное приложение для проигрывания видеороликов с YouTube, которое не требует Google Play Services для работы. Требуется Android 4.0+

#### Идейные клиенты, которые выступают за приватность

> [!WARNING]
> Для работы данных приложений требуются инстансы. Они могут быть заблокированы и требовать [разблокировки](features.md#разблокировать-свои-ресурсы).

- [FreeTube Android](https://github.com/MarmadileManteater/FreeTubeAndroid) - клиент YouTube, использующий Invidious API для передачи данных и видео с YouTube. Требуется Android 7.0+
- [Clipious](https://github.com/lamarios/clipious) - клиент для Invidious, пользовательского интерфейса YouTube, ориентированного на конфиденциальность. Подеррживает Sponsorblock и ReturnYouTubeDislike. Заявлена поддержка интерфеса для **телевизоров**. Требуется Android 4.1+
- [LibreTube](https://github.com/libre-tube/LibreTube) - клиент, использующий [API Piped](https://github.com/TeamPiped/Piped) для отображения содержимого каналов и воспроизведения контента, не требует наличия учетной записи YouTube и сервисов Google.

#### Ещё варианты

- [VueTube](https://github.com/pixkk/VueTube) - клиент YouTube построенный на базе Vue. Есть поддержка Sponsorblock и ReturnYouTubeDislike. Требуется Android 5.0+ (возможно не поддерживается Android 12.1+)
- [Namida](https://github.com/namidaco/namida) - красивый и многофункциональный проигрыватель музыки и видео с поддержкой YouTube.

#### Проприетарные программы

- [PureTuber](https://play.google.com/store/apps/details?id=free.tube.premium.advanced.tuber) – это клиент для YouTube, за основу которого был взят NewPipe. Новый интерфейс и добавлена возможность входа в google-аккаунт. Требуется Android 4.4+
- [GreenTuber](https://play.google.com/store/apps/details?id=by.green.tuber&hl=en) - YouTube с блокировщиком рекламы. Требуется Android 6.0+

## <a id="dns">Про DNS</a>

**DNS** - это система доменных имен (Domain Name System), с помощью которой любому IP (например, `108.177.119.91`) можно присвоить доменное имя (например, `youtube.com`). DNS имеет собственные сервера и использует иерархическую систему для запросов.

### Перехват DNS

**Перехват DNS** — вредоносная практика, которая заключается в перенаправлении DNS-запросов на неправильный DNS-сервер. В итоге, когда запрос обрабатывается, вы получаете неверные результаты.

Другими словами, если ваши запросы отправляются на "плохой" DNS-сервер, он не возвращает вам в ответ адрес нужного ресурса. Чтобы избежать этого используются технологии DoT, DoH, DoQ и другие способы защиты DNS-трафика.

Чтобы определить какой DNS-сервер вы используете сейчас, откройте этот [сайт](https://browserleaks.com/dns).

### <a id="proxy-dns">Проксирующие DNS</a>

Чтобы использовать некоторые ресурсы, которые заблокированы извне можно использовать проксирующие DNS - они скрывают ваше местоположение от некоторых ресурсов.

В теории, такие DNS можно установить в ByeByeDPI в формате IPv4 и пропускать трафик к заблокированному ресурсу через ByeByeDPI, но это не сильно рационально. Лучшим вариантом будет установить DoH на уровне браузера. Не стоит использовать такие DNS для всей системы, так как, например, Comss DNS иногда не выдерживает нагрузки и отключается. Если такой DNS будет работать для всей системы - у вас пропадёт интернет.

Вот к чему можно получить доступ, используя  [Comss DNS](https://www.comss.ru/page.php?id=7315): вы можете пользоваться ИИ-сервисами (ChatGPT и Sora, Microsoft Copilot, GitHub Copilot, xAI Grok, Google Gemini и Claude AI), или устанавливать обновления антивирусов, инсайдерские сборки и обновления Windows, а также играть в Brawl Stars и сетевые режимы Doom Eternal в России.

## <a id="other-options">Другие варианты ускорения серверов</a>

> [!TIP]
> ByeDPI или zapret? Если вы хотите, чтобы устройства внутри локальной сети могли подключаться к вашему компьютеру - используйте ByeDPI и читайте [инструкцию](features.md#distribute) по предоставлению доступа к ByeByeDPI - действия почти идентичные.

### <a id="other-android">На Android</a>

#### Модули Magisk для Android (нужен root)

- [ZDT&D Magisk Module](https://github.com/GAME-OVER-op/ZDT-D) от GAME-OVER-op (предпочтительнее)
- [zapret-magisk](https://github.com/ImMALWARE/zapret-magisk) от ImMALWARE

### <a id="other-windows">На Windows</a>

#### Сборки zapret

- [YTDisBystro](https://ntc.party/t/%D1%81%D0%B1%D0%BE%D1%80%D0%BA%D0%B0-ytdisbystro-%D0%BD%D0%B0-%D0%BE%D1%81%D0%BD%D0%BE%D0%B2%D0%B5-zapret-%D0%B4%D0%BB%D1%8F-windows-%D0%BE%D0%B1%D1%81%D1%83%D0%B6%D0%B4%D0%B5%D0%BD%D0%B8%D0%B5/13251) сборка zapret от KDS (подходит для 32-х битных систем, Windows 7 в том числе).
- [zapret-discord-youtube](https://github.com/Flowseal/zapret-discord-youtube) сборка zapret от Flowseal (простое решение без излишеств).

#### Приложения с графическим интерфейсом

- [goodbyeDPI-UI](https://github.com/Storik4pro/goodbyeDPI-UI) от Storik4pro (комбайн для zapret, ByeDPI, GoodbyeDPI и SpoofDPI).
- [ByeDPI Manager](https://github.com/romanvht/bdmanager/releases) от romanvht. Небольшая утилита, упрощающая работу с ByeDPI на Windows (подходит для некоторых версий Windows 7).

#### Оригинальные утилиты

- [zapret](https://github.com/bol-van/zapret) от bol-van
- [ByeDPI](https://github.com/hufrea/byedpi) от hufrea (в теории версия [byedpi-x86-cygwin.zip](https://github.com/hufrea/byedpi/issues/219#issuecomment-2559707231) способна работать даже на Windows XP)

#### Инструкции к оригинальным утилитам

> [!CAUTION]
> В ByeDPI нет подбора стратегий - найти рабочую стратегию необходимо самостоятельно (например, при помощи подбора в ByeByeDPI).

- [zapret](https://github.com/bol-van/zapret?tab=readme-ov-file#%D0%B1%D1%8B%D1%81%D1%82%D1%80%D1%8B%D0%B9-%D1%81%D1%82%D0%B0%D1%80%D1%82)
- [ByeDPI](byedpi-guide-windows.md)

### <a id="other-linux">На Linux</a>

##### Скрипты для автоматической установки

> [!CAUTION]
> Данные скрипты не рекомендуются для использования. Настраивайте оригинальные утилиты

- [zapret.installer](https://github.com/Snowy-Fluffy/zapret.installer) от Snowy-Fluffy
- [zapret-discord-youtube-linux](https://github.com/Sergeydigl3/zapret-discord-youtube-linux) от Sergeydigl3
- [Byedpi-Setup](https://github.com/fatyzzz/Byedpi-Setup) от fatyzzz

#### Оригинальные утилиты

- [zapret](https://github.com/bol-van/zapret) от bol-van
- [ByeDPI](https://github.com/hufrea/byedpi) от hufrea
- [youtubeUnblock](https://github.com/Waujito/youtubeUnblock) от Waujito

#### Инструкции к оригинальным утилитам

> [!CAUTION]
> В ByeDPI нет подбора стратегий - найти рабочую стратегию необходимо самостоятельно (например, при помощи подбора в ByeByeDPI).

- [zapret](https://github.com/bol-van/zapret?tab=readme-ov-file#%D0%B1%D1%8B%D1%81%D1%82%D1%80%D1%8B%D0%B9-%D1%81%D1%82%D0%B0%D1%80%D1%82)
- [zapret](https://www.youtube.com/watch?v=FdDC9R7gL-Y&t=53s) видеоинструкция
- [ByeDPI](https://youtu.be/zlWMp8IlGCU?si=xZ-xAlts09Atugvq) видеоинструкция

### <a id="other-router">На роутере</a>

- [Инструкция](https://github.com/bol-van/zapret/blob/master/docs/quick_start.md) на оригинальный zapret (OpenWrt)
- [Инструкция](https://github.com/remittor/zapret-openwrt) на zapret‐openwrt (zapret с интерфейсом для OpenWrt)
- [Инструкция](https://github.com/Anonym-tsk/nfqws-keenetic) на nfqws (программа из состава zapret подходит для Keenetic / OpenWrt / Netcraze / Padavan)
- [Инструкция](https://habr.com/ru/articles/834826/) на nfqws (программа из состава zapret подходит для Keenetic)
- [ByeDPI для OpenWrt](https://github.com/spvkgn/ByeDPI-OpenWrt)
- [Инструкция](https://habr.com/ru/articles/856312/) на ByeDPI (OpenWrt)
- [Инструкция](https://lsetc.ru/ustanovka-youtubeunblock-na-openwrt/) по установке youtubeUnblock на OpenWrt
- [Инструкция](https://habr.com/ru/articles/838452/) на ByeDPI для мощных MikroTik

### <a id="other-home-server">На домашнем сервере (постоянно включенном устройстве)</a>

- Можно подключаться к ByeDPI, который будет развёрнут на вашем ПК
- [Можно подключаться](features.md#distribute) к телефону, на котором запущен ByeByeDPI
- [ByeDPI на одноплатном компьютере](https://habr.com/ru/articles/870254/)
- [youtubeUnblock на одноплатном компьютере](https://habr.com/ru/articles/871460/)
- [zapret в контейнере c Shadowsocks](https://github.com/vernette/ss-zapret) для сервера
- [zapret на одноплатном компьютере](https://habr.com/ru/articles/833508/)

### <a id="other-mac">На Mac</a>

> [!CAUTION]
> Выполняйте инструкции на свой страх и риск!

> [!TIP]
> Настроить ByeDPI проще

- [ByeDPI](https://github.com/hufrea/byedpi) от hufrea
- [zapret](https://github.com/bol-van/zapret/blob/master/docs/bsd.md#macos) от bol-van

[Видеоинструкция](https://youtu.be/zlWMp8IlGCU?si=xZ-xAlts09Atugvq) по установке ByeDPI *на Linux*

Так как автор инструкции не имеет устройства с MacOS, он может только предположить, что вместо команд которые показаны автором видео необходимо использовать другие:

- Установите инструменты командной строки Xcode

```
xcode-select --install
```

-  Установите Homebrew (менеджер пакетов для macOS)

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

- Установите необходимые инструменты

```
brew install git gcc make binutils
```

- Склонируйте репозиторий

```
git clone https://github.com/hufrea/byedpi.git
```

- Перейдите в папку

```
cd byedpi
```

- Скомпилируйте

```
make
```

- Сделайте исполняемым  `ciadpi`

```
chmod +x ciadpi
```

- Запустите

> [!WARNING]
> [] - квадратные скобочки писать не нужно. Если вы не можете использовать ByeByeDPI - перебирайте стратегии из [списка](ALL.TXT)

```
./ciadpi [стратегия, которая работает на телефоне в приложении ByeByeDPI в вашей сети]
```

Чтобы проверить работу ByeDPI, [установите Firefox](https://www.mozilla.org/en-US/firefox/mac/) как и автор видео, и проверьте работу сервисов там. Если всё хорошо работает - в последствии можно будет использовать приложения по типу FoXray, [V2RayXS](https://github.com/tzmax/V2RayXS), [nekoray](https://github.com/Mahdi-zarei/nekoray).

> [!CAUTION]
> Для запуска в следующие разы необходимо указывать полный путь до папки с файлом, например: `/Users/you/apps/byedpi`

Чтобы добавить в автозапуск

- Создайте plist-файл для LaunchAgent

Создайте файл .plist в каталоге ~/Library/LaunchAgents/

```
nano ~/Library/LaunchAgents/com.user.byedpi.plist
```

- Настройка файла plist. **УКАЖИТЕ ПУТЬ ДО ФАЙЛА ciadpi**

```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
<dict>
  <!-- Unique identifier for your service -->
  <key>Label</key>
  <string>com.user.byedpi</string>

  <!-- Path to your executable -->
  <key>Program</key>
  <string>/УКАЖИТЕ/ПОЛНЫЙ/ПУТЬ/ciadpi</string>

  <!-- Command-line arguments -->
  <key>ProgramArguments</key>
  <array>
    <string>/УКАЖИТЕ/ПОЛНЫЙ/ПУТЬ/ciadpi</string>
    <string>АРГУМЕНТ СТРАТЕГИИ 1</string>
    <string>АРГУМЕНТ СТРАТЕГИИ 2</string>
    <string>ОСТАЛЬНЫЕ АРГУМЕНТЫ ТАКЖЕ ПО ПОРЯДКУ СВЕРХУ ВНИЗ</string>
  </array>

  <!-- Run at login/startup -->
  <key>RunAtLoad</key>
  <true/>

  <!-- Keep the process alive if it crashes -->
  <key>KeepAlive</key>
  <true/>
</dict>
</plist>
```

- Исправьте разрешения и загрузите службу

```
chmod 644 ~/Library/LaunchAgents/com.user.byedpi.plist
```

```
launchctl load ~/Library/LaunchAgents/com.user.byedpi.plist
```

```
launchctl start com.user.ciadpi
```

Чтобы удалить выполните:

```
launchctl unload ~/Library/LaunchAgents/com.user.byedpi.plist
```

```
rm ~/Library/LaunchAgents/com.user.byedpi.plist
```

## <a id="ui-editor">"Стандартный редактор" - нужен ли?</a>

Чтобы разрабатывать стратегию (а настройки в графическом редакторе это и есть данный процесс), необходимо разбираться в работе сетей и понимать за что отвечает каждый пункт настроек досконально изучив [документацию](https://github.com/hufrea/byedpi). Тем, кто изучил документацию, не нужен графический редактор, потому что он не отображает всех аргументов, а делает это лишь частично.

"Стандартный редактор" **не нужен**. Тыкать наугад - плохая тактика.

## <a id="universal">Универсальная стратегия</a>

Если вам показалась сложной настройка или у вас ничего не работает - используйте VPN. Или смотрите VK Видео и Rutube - это отличные платформы.
