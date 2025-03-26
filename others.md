# Другое

1. [Клиенты YouTube](#клиенты)
2. [Про DNS](#dns)
3. ["Стандартный редактор" - нужен ли?](#ui-editor)
4. [Другие варианты ускорения серверов](#other-options)
5. [Универсальная стратегия](#universal)

## <a id="клиенты">Клиенты YouTube</a>


Если вас по каким-то причинам не устраивает оригинальное приложение YouTube, вот несколько альтернативных:

- [YouTube for Androuid TV](https://play.google.com/store/apps/details?id=com.google.android.youtube.tv) - если у вас телевизор.
- YouTube ReVanced Extended - если у вас проблемы с QUIC.
- YouTube ReVanced. Вот ссылка на [Revanced Manager](https://revanced.net/revanced-manager) - приложение для удобного скачивания и обновления ReVanced и MicroG. [revanced.app](https://revanced.app/) - Официальный сайт ReVanced
- [PureTuber](https://play.google.com/store/apps/details?id=free.tube.premium.advanced.tuber) – это клиент для YouTube, за основу которого был взят другой клиент - NewPipe. Новый интерфейс и добавлена возможность входа в google аккаунт.
- [VancedTuber](https://vanced-official.com/) – это клиент для YouTube на основе NewPipe от авторов PureTuber, упрощенная версия клиента выше.
- [NewPipe](https://github.com/TeamNewPipe/NewPipe/releases) -  клиент для YouTube, который не использует каких-либо библиотек, зависящих от Google или каких-либо Youtube API. Отсутствует функция авторизации в google аккаунт.

### Для продвинутых

Для установки YouTube ReVanced и YouTube ReVanced Extended рекомендуется патчить приложение самостоятельно:

- [YouTube ReVanced Manager](https://github.com/ReVanced/revanced-manager)
- [RVX Manager](https://github.com/inotia00/revanced-manager)

## <a id="dns">Про DNS</a>

**DNS** - это система доменных имен (Domain Name System), с помощью которой любому IP (например, `108.177.119.91`) можно присвоить доменное имя (например, `youtube.com`). DNS имеет собственные сервера и использует иерархическую систему для запросов.

### Утечка DNS

**Утечка DNS** (Domain Name System) — ситуация, когда ваше устройство неожиданно отправляет DNS-запросы через серверы, которые отличаются от заданных вами в настройках сетевого оборудования.

Другими словами, если ваши запросы отправляются на "плохой" DNS-сервер, он не возвращает вам в ответ адрес желаемого ресурса, чтобы избежать этого используются технологии DoT, DoH, DoQ и другие способы защиты DNS-трафика.

Чтобы определить возможную утечку, откройте этот [сайт](https://browserleaks.com/dns).

### <a id="proxy-dns">Проксирующие DNS</a>

Чтобы использовать некоторые ресурсы, которые заблокированы извне можно использовать проксирующие DNS - они скрывают ваше местоположение от некоторых ресурсов.

В теории, такие DNS можно установить в ByeByeDPI в формате IPv4 и пропускать трафик к заблокированному ресурсу через ByeByeDPI, но это не сильно рационально. Лучшим вариантом будет установить DoH на уровне браузера. Не стоит использовать такие DNS для всей системы, так как, например, Comss DNS иногда не выдерживает нагрузки и отключается. Если такой DNS будет работать для всей системы - у вас пропадёт интернет.

Вот к чему можно получить доступ, используя  [Comss DNS](https://www.comss.ru/page.php?id=7315): вы можете пользоваться ИИ-сервисами (ChatGPT и Sora, Microsoft Copilot, GitHub Copilot, xAI Grok, Google Gemini и Claude AI), или устанавливать обновления антивирусов, инсайдерские сборки и обновления Windows, а также играть в Brawl Stars и сетевые режимы Doom Eternal в России.

## <a id="ui-editor">"Стандартный редактор" - нужен ли?</a>

Чтобы разрабатывать стратегию (а настройки в графическом редакторе это и есть данный процесс), необходимо разбираться в работе сетей и понимать за что отвечает каждый пункт настроек досконально изучив [документацию](https://github.com/hufrea/byedpi). Тем, кто изучил документацию, не нужен графический редактор, потому что он не отображает всех аргументов, а делает это лишь частично.

"Стандартный редактор" **не нужен**. Тыкать наугад - плохая тактика.

## <a id="other-options">Другие варианты ускорения серверов</a>

### Модули Magisk для Android (нужен root)

- [zapret-magisk](https://github.com/ImMALWARE/zapret-magisk) от ImMALWARE
- [ZDT&D Magisk Module](https://github.com/GAME-OVER-op/ZDT-D) от GAME-OVER-op

> [!TIP]
> ByeDPI или zapret? Если вы хотите, чтобы устройства внутри локальной сети могли подключаться к вашему компьютеру - используйте ByeDPI и читайте [инструкцию](features.md#раздача) по предоставлению доступа к ByeByeDPI - действия почти идентичные.

### Простые варианты для ПК

#### Сборки **zapret** без интерфейса

- [YTDisBystro](https://ntc.party/t/%D1%81%D0%B1%D0%BE%D1%80%D0%BA%D0%B0-ytdisbystro-%D0%BD%D0%B0-%D0%BE%D1%81%D0%BD%D0%BE%D0%B2%D0%B5-zapret-%D0%B4%D0%BB%D1%8F-windows-%D0%BE%D0%B1%D1%81%D1%83%D0%B6%D0%B4%D0%B5%D0%BD%D0%B8%D0%B5/13251) от KDS (подходит для 32-х битных систем, Windows 7 в том числе)
- [zapret-discord-youtube](https://github.com/Flowseal/zapret-discord-youtube) от Flowseal (простое решение без излишеств)
- [zapret.installer](https://github.com/Snowy-Fluffy/zapret.installer) от Snowy-Fluffy. Сборка zapret для Линукс

#### Приложения с графическим интерфейсом

- [goodbyeDPI-UI](https://github.com/Storik4pro/goodbyeDPI-UI) от Storik4pro (комбайн для zapret, ByeDPI и GoodbyeDPI)
- [ByeDPI Manager](https://github.com/romanvht/bdmanager/releases) от romanvht

### Оригинальные утилиты

- [zapret](https://github.com/bol-van/zapret) от болвана (для Windows / Linux / OpenWrt / Entware / Mac)
- [ByeDPI](https://github.com/hufrea/byedpi) от hufrea (для Windows - в теории версия [byedpi-x86-cygwin.zip](https://github.com/hufrea/byedpi/issues/219#issuecomment-2559707231) способна работать даже на Windows XP  / Linux / OpenWrt / Mac)
- [youtubeUnblock](https://github.com/Waujito/youtubeUnblock) от Waujito (для Linux / OpenWrt / Entware)

#### Инструкции к оригинальным утилитам

> [!TIP]
> На Mac проще всего запустить ByeDPI. Необходимо выполнить те же самые действия, как в этом [видео](https://youtu.be/zlWMp8IlGCU?si=xZ-xAlts09Atugvq).

> [!CAUTION]
> В ByeDPI нет подбора стратегий - найти рабочую стратегию необходимо самостоятельно (например, при помощи подбора в ByeByeDPI).

- [zapret](https://github.com/bol-van/zapret?tab=readme-ov-file#%D0%B1%D1%8B%D1%81%D1%82%D1%80%D1%8B%D0%B9-%D1%81%D1%82%D0%B0%D1%80%D1%82) для Windows / Linux / OpenWrt
- [ByeDPI](byedpi-guide-windows.md) для Windows
- [zapret](https://github.com/bol-van/zapret/blob/master/docs/bsd.md) для Mac / BSD-систем
- [zapret](https://www.youtube.com/watch?v=FdDC9R7gL-Y&t=53s) видеоинструкция для Linux
- [ByeDPI](https://youtu.be/zlWMp8IlGCU?si=xZ-xAlts09Atugvq) видеоинструкция для Linux (скорее всего такой же принцип для Mac)

### Решения для роутеров

- [Инструкция](https://github.com/bol-van/zapret/blob/master/docs/quick_start.md) на оригинальный zapret (OpenWrt)
- [Инструкция](https://github.com/Anonym-tsk/nfqws-keenetic) на nfqws (программа из состава zapret подходит для Keenetic / OpenWrt)
- [Инструкция](https://habr.com/ru/articles/834826/) на nfqws (программа из состава zapret подходит для Keenetic)
- [Инструкция](https://habr.com/ru/articles/856312/) на ByeDPI (OpenWrt)
- [Инструкция](https://habr.com/ru/articles/838452/) для мощных MikroTik

### При помощи домашнего прокси-сервера:

- [Решаем проблему устаревания кэширующих серверов. Смотрим на телевизоре. Не VPN](https://habr.com/ru/articles/870254/)
- [Ускоряем кэш серверы YouTube. Не VPN](https://habr.com/ru/articles/871460/)

## <a id="universal">Универсальная стратегия</a>

Если вам показалась сложной настройка или у вас ничего не работает - используйте VPN. Или смотрите VK Видео и Rutube - это отличные платформы.
