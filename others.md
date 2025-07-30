# Другое

1. [Клиенты YouTube](#клиенты)
2. [Проксирующие DNS](#proxy-dns)
3. [Другие варианты ускорения серверов](#other-options)
     - [На Android](#other-android)
     - [На Windows](#other-windows)
     - [На Linux](#other-linux)
     - [На роутере](#other-router)
     - [На домашнем сервере (постоянно включенном устройстве)](#other-home-server)
     - [На Mac](#other-mac)
     - [На iOS](#other-iphone)
4. ["Стандартный редактор" - нужен ли?](#ui-editor)
5. [Универсальная стратегия](#universal)

## <a id="клиенты">Клиенты YouTube</a>

Если вас по каким-то причинам не устраивает оригинальное приложение YouTube, вот несколько альтернативных:

#### Для телевизоров и приставок

- [YouTube for Androuid TV](https://play.google.com/store/apps/details?id=com.google.android.youtube.tv) - официальное приложение YouTube для управления пультом. Требуется Android 7.0+
- [SmartTube](https://github.com/yuliskov/SmartTube) - единственный клиент с поддержкой прокси. Требуется Android 4.3+

#### YouTube с патчами

- YouTube ReVanced. [Revanced Manager](https://revanced.app/download) - приложение для удобного скачивания и обновления ReVanced и MicroG. [revanced.app](https://revanced.app/) - Официальный сайт ReVanced. Требуется Android 8.0+
- YouTube ReVanced Extended - если у вас проблемы с QUIC. Требуется Android 8.0+

> [!TIP]
> Для установки YouTube ReVanced и YouTube ReVanced Extended рекомендуется патчить приложение самостоятельно:

- [YouTube ReVanced Manager](https://github.com/ReVanced/revanced-manager)
- [RVX Manager](https://github.com/inotia00/revanced-manager)

#### NewPipe и его вариации

- [NewPipe](https://github.com/TeamNewPipe/NewPipe/releases) - клиент для YouTube, который не использует каких-либо библиотек, зависящих от Google. Отсутствует функция авторизации в google аккаунт. Требуется Android 5.0+
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
> Для работы данных приложений требуются инстансы. Они могут быть заблокированы иначе чем YouTube и требовать [разблокировки](features.md#разблокировать-свои-ресурсы) отдельно.

- [FreeTube Android](https://github.com/MarmadileManteater/FreeTubeAndroid) - клиент YouTube, использующий Invidious API для передачи данных и видео с YouTube. Требуется Android 7.0+
- [Clipious](https://github.com/lamarios/clipious) - клиент для Invidious, пользовательского интерфейса YouTube, ориентированного на конфиденциальность. Подеррживает Sponsorblock и ReturnYouTubeDislike. Заявлена поддержка интерфейса для **телевизоров**. Требуется Android 4.1+
- [LibreTube](https://github.com/libre-tube/LibreTube) - клиент, использующий [API Piped](https://github.com/TeamPiped/Piped) для отображения содержимого каналов и воспроизведения контента, не требует наличия учетной записи YouTube и сервисов Google.
- [Mini YouTube](https://github.com/monobogdan/selfeco) - клиент YouTube из состава приложений SelfEco. Использует Invidous API. **Требуется Android 2.2+**. Также существует [форк](https://github.com/tinelix/selfeco-plus), с заявленной поддержкой HTTP-прокси для YouTube, однако собирать приложение нужно самостоятельно.

#### Ещё варианты

- [VueTube](https://github.com/pixkk/VueTube) - клиент YouTube построенный на базе Vue. Есть поддержка Sponsorblock и ReturnYouTubeDislike. Требуется Android 5.0+ (возможно не поддерживается Android 12.1+)
- [Namida](https://github.com/namidaco/namida) - красивый и многофункциональный проигрыватель музыки и видео с поддержкой YouTube.

#### Проприетарные программы

- [PureTuber](https://play.google.com/store/apps/details?id=free.tube.premium.advanced.tuber) – это клиент для YouTube, за основу которого был взят NewPipe. Новый интерфейс и добавлена возможность входа в google-аккаунт. Требуется Android 4.4+
- [GreenTuber](https://play.google.com/store/apps/details?id=by.green.tuber&hl=en) - YouTube с блокировщиком рекламы. Требуется Android 6.0+

## <a id="proxy-dns">Проксирующие DNS</a>

> [!CAUTION]
> Будьте осторожны при использовании различных DNS. Используйте только те DNS-сервера, в надёжности и безопасности которых вы уверены.

Чтобы использовать некоторые ресурсы, которые заблокированы извне можно использовать проксирующие DNS - они скрывают ваше местоположение от некоторых ресурсов.

В теории, такие DNS можно установить в ByeByeDPI в формате IPv4 и пропускать трафик к заблокированному ресурсу через ByeByeDPI, но это не сильно рационально. Лучшим вариантом будет установить DoH на уровне браузера. Не стоит использовать такие DNS для всей системы, так как, например, Comss DNS иногда не выдерживает нагрузки и отключается. Если такой DNS будет работать для всей системы - у вас пропадёт интернет.

Вот к чему можно получить доступ, используя [Comss DNS](https://www.comss.ru/page.php?id=7315): вы можете пользоваться ИИ-сервисами (ChatGPT и Sora, Microsoft Copilot, GitHub Copilot, xAI Grok, Google Gemini и Claude AI), или устанавливать обновления антивирусов, инсайдерские сборки и обновления Windows, а также играть в Brawl Stars и сетевые режимы Doom Eternal в России.

## <a id="other-options">Другие варианты ускорения серверов</a>

> [!CAUTION]
> Используйте любые решения на свой страх и риск. Авторы руководства не отвечают за последствия и возможный вред от использования любого программного обеспечения, которое упомянуто в данном мануале.

> [!TIP]
> ByeDPI или zapret? Если вы хотите, чтобы устройства внутри локальной сети могли подключаться к вашему компьютеру - используйте ByeDPI и читайте [инструкцию](features.md#distribute) по предоставлению доступа к ByeByeDPI - действия почти идентичные.

### <a id="other-android">На Android</a>

#### Модули Magisk для Android (нужен root)

- [ZDT&D Magisk Module](https://github.com/GAME-OVER-op/ZDT-D) от GAME-OVER-op
- [zapret-magisk](https://github.com/ImMALWARE/zapret-magisk) от ImMALWARE
- [zaprett](https://github.com/egor-white/zaprett) от egor-white и приложение [zaprett-app](https://github.com/CherretGit/zaprett-app) от CherretGit для работы с ним

### <a id="other-windows">На Windows</a>

#### Сборки zapret

- [zapret-discord-youtube](https://github.com/Flowseal/zapret-discord-youtube) сборка zapret от Flowseal (простое решение без излишеств).

#### Приложения с графическим интерфейсом

- [goodbyeDPI-UI](https://github.com/Storik4pro/goodbyeDPI-UI) от Storik4pro (комбайн для zapret, ByeDPI, GoodbyeDPI и SpoofDPI).
- [ByeDPI Manager](https://github.com/romanvht/bdmanager/releases) от romanvht. Небольшая утилита, упрощающая работу с ByeDPI на Windows (подходит для некоторых версий Windows 7).

#### Оригинальные утилиты

- [zapret](https://github.com/bol-van/zapret) от bol-van
- [ByeDPI](https://github.com/hufrea/byedpi) от hufrea (в теории версия [byedpi-x86-cygwin.zip](https://github.com/hufrea/byedpi/issues/219#issuecomment-2559707231) способна работать даже на Windows XP)

#### Инструкции к оригинальным утилитам

> [!CAUTION]
> В ByeDPI нет подбора стратегий - найти рабочую стратегию необходимо самостоятельно (например, при помощи подбора в [ByeByeDPI](https://github.com/romanvht/ByeByeDPI) или [ByeDPI Manager](https://github.com/romanvht/ByeDPIManager)).

- [zapret](https://github.com/bol-van/zapret?tab=readme-ov-file#%D0%B1%D1%8B%D1%81%D1%82%D1%80%D1%8B%D0%B9-%D1%81%D1%82%D0%B0%D1%80%D1%82)
- [ByeDPI](byedpi-guide-windows.md)

### <a id="other-linux">На Linux</a>

##### Скрипты для автоматической установки

> [!CAUTION]
> Данные скрипты не рекомендуются для использования. Настраивайте оригинальные утилиты

- [zapret.installer](https://github.com/Snowy-Fluffy/zapret.installer) от Snowy-Fluffy
- [zapret-discord-youtube-linux](https://github.com/Sergeydigl3/zapret-discord-youtube-linux) от Sergeydigl3
- [zapret4rocket](https://github.com/IndeecFOX/zapret4rocket) от IndeecFOX
- [Byedpi-Setup](https://github.com/fatyzzz/Byedpi-Setup) от fatyzzz

#### Оригинальные утилиты

- [zapret](https://github.com/bol-van/zapret) от bol-van
- [zapret в контейнере](https://github.com/vernette/ss-zapret) c Shadowsocks и SOCKS5 от vernette
- [ByeDPI](https://github.com/hufrea/byedpi) от hufrea
- [контейнер с ByeDPI](https://hub.docker.com/r/tazihad/byedpi) от tazihad
- [youtubeUnblock](https://github.com/Waujito/youtubeUnblock) от Waujito

#### Инструкции к оригинальным утилитам

> [!CAUTION]
> В ByeDPI нет подбора стратегий - найти рабочую стратегию необходимо самостоятельно (например, при помощи подбора в ByeByeDPI).

- [zapret](https://github.com/bol-van/zapret?tab=readme-ov-file#%D0%B1%D1%8B%D1%81%D1%82%D1%80%D1%8B%D0%B9-%D1%81%D1%82%D0%B0%D1%80%D1%82)
- [zapret](https://www.youtube.com/watch?v=FdDC9R7gL-Y&t=53s) видеоинструкция
- [ByeDPI](https://github.com/hufrea/byedpi/tree/main/dist/linux)

### <a id="other-router">На роутере</a>

#### OpenWrt

- [Оригинальный zapret](https://github.com/bol-van/zapret/blob/master/docs/quick_start.md)
- [zapret‐openwrt](https://github.com/remittor/zapret-openwrt) - zapret с интерфейсом
- [nfqws](https://github.com/Anonym-tsk/nfqws-keenetic) - программа из состава zapret. Есть инструкция для Keenetic / OpenWrt / Netcraze / Padavan
- [ByeDPI для OpenWrt](https://github.com/spvkgn/ByeDPI-OpenWrt)
- [ByeDPI + Redsocks](https://habr.com/ru/articles/856312/)
- [youtubeUnblock](https://lsetc.ru/ustanovka-youtubeunblock-na-openwrt/)

> [!TIP]
> Можно использовать [пакет ByeDPI](https://github.com/spvkgn/ByeDPI-OpenWrt) в качестве кастомного outbound'a в [podkop](https://github.com/itdoginfo/podkop), чтобы управлять трафиком через sign-box 

#### Keenetic

- [nfqws](https://github.com/Anonym-tsk/nfqws-keenetic) - программа из состава zapret. Есть инструкция для Keenetic / OpenWrt / Netcraze / Padavan
- [zapret](https://github.com/AlexFBG/zapret)
- [nfqws](https://habr.com/ru/articles/834826/) - программа из состава zapret. Инструкция для Keenetic

#### MikroTik

- [ByeDPI](https://habr.com/ru/articles/838452/) - статья с инструкцией
- [Контейнеры](https://hub.docker.com/u/wiktorbgu) с tpws из состава zapret и ByeDPI. В tpws нет возможности использовать UDP

### <a id="other-home-server">На домашнем сервере (постоянно включенном устройстве)</a>

- Можно подключаться к ByeDPI, который будет развёрнут на вашем ПК
- [Можно подключаться](features.md#distribute) к телефону, на котором запущен ByeByeDPI
- [ByeDPI на одноплатном компьютере](https://habr.com/ru/articles/870254/)
- [youtubeUnblock на одноплатном компьютере](https://habr.com/ru/articles/871460/)
- [zapret в контейнере](https://github.com/vernette/ss-zapret) c Shadowsocks и SOCKS5
- [zapret на одноплатном компьютере](https://habr.com/ru/articles/833508/)
- [контейнер с ByeDPI](https://hub.docker.com/r/tazihad/byedpi)
- [ByeDPI на Synology](https://bafista.ru/ustanovka-byedpi-v-kontejner-docker-na-synology/) или [ByeDPI на TerraMaster](https://bafista.ru/ustanovka-byedpi-v-kontejner-docker-na-terramaster/)

### <a id="other-mac">На Mac</a>

> [!CAUTION]
> Выполняйте инструкции на свой страх и риск!

> [!TIP]
> Настроить ByeDPI проще. Как в варианте с контейнером, так и в варианте с нативной установкой.

- [ByeDPI](https://github.com/hufrea/byedpi) от hufrea
- [zapret](https://github.com/bol-van/zapret/blob/master/docs/bsd.md#macos) от bol-van

#### Контейнер с ByeDPI

[контейнер с ByeDPI](https://hub.docker.com/r/tazihad/byedpi) от tazihad

#### Нативная установка

[Инструкция](https://github.com/hufrea/byedpi/tree/main/dist/linux) по установке ByeDPI *на Linux*

Так как автор инструкции не имеет устройства с MacOS, он может только предположить, что необходимо выполнить следующие шаги:

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

Чтобы проверить работу ByeDPI, [установите Firefox](https://www.mozilla.org/en-US/firefox/mac/) и проверьте работу сервисов там, подключившись к SOCKS5-прокси ByeDPI. Если всё хорошо работает - в последствии можно будет использовать приложения по типу FoXray, [V2RayXS](https://github.com/tzmax/V2RayXS), [nekoray](https://github.com/Mahdi-zarei/nekoray).

> [!CAUTION]
> На данном этапе установка завершена.
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

Чтобы удалить, выполните:

```
launchctl unload ~/Library/LaunchAgents/com.user.byedpi.plist
```

```
rm ~/Library/LaunchAgents/com.user.byedpi.plist
```

## <a id="other-iphone">На iOS</a>

Решений по обходу DPI конкретно на iOS не существует и, скорее всего, никогда не появится.

Варианты для пользователей iOS:

- Использовать VPN. Не требует особых навыков, усилий и знаний
- Раздать доступ к ByeByeDPI с Android-устройства. Данный вариант подойдёт, если есть устройство на Android с настроенным ByeByeDPI. Подробная инструкция [здесь](features.md#раздача-интернета-с-byebyedpi-локальный-прокси)
- Использовать решения по [обходу DPI на роутере](#other-router)
- Использовать решения по [обходу DPI на домашнем сервере](#other-home-server) (в качестве сервера может выступать ПК)

> [!NOTE]
> Если приобрести белый IP у провайдера, то можно будет настроить VPN-туннель до роутера и выходит в интернет с телефона через роутер с настроенным средством обхода

## <a id="ui-editor">Стандартный редактор" - нужен ли?</a>

Чтобы разрабатывать стратегию (а настройки в графическом редакторе это и есть данный процесс), необходимо разбираться в работе сетей и понимать за что отвечает каждый пункт настроек досконально изучив [документацию](https://github.com/hufrea/byedpi). Тем, кто изучил документацию, не нужен графический редактор, потому что он не отображает всех аргументов, а делает это лишь частично.

"Стандартный редактор" **не нужен**. Тыкать наугад - плохая тактика.

## <a id="universal">Универсальная стратегия</a>

Если вам показалась сложной настройка или у вас ничего не работает - используйте VPN. Или смотрите VK Видео и Rutube - это отличные платформы.
