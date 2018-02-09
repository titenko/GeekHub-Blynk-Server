# GeekHub-Blynk-Server
Платформа с приложением для iOS и Android для управления Arduino, ESP8266, Raspberry Pi и других плат микроконтроллеров через Интернет.

# Что такое Blynk?
Blynk - это платформа с приложениями для iOS и Android для управления Arduino, ESP8266, Raspberry Pi и подобных через Интернет.
Вы можете легко создавать графические интерфейсы для всех своих проектов, просто перетаскивая виджеты. Если вам нужна дополнительная информация, перейдите по следующим ссылкам:
* [Blynk site](https://www.blynk.cc)
* [Blynk docs](http://docs.blynk.cc)
* [Blynk community](https://community.blynk.cc)
* [Blynk Examples generator](https://examples.blynk.cc)
* [Facebook](http://www.fb.com/blynkapp)
* [Twitter](http://twitter.com/blynk_app)
* [App Store](https://itunes.apple.com/us/app/blynk-control-arduino-raspberry/id808760481?ls=1&mt=8)
* [Google Play](https://play.google.com/store/apps/details?id=cc.blynk)
* [Blynk library](https://github.com/blynkkk/blynk-library)
* [Kickstarter](https://www.kickstarter.com/projects/167134865/blynk-build-an-app-for-your-arduino-project-in-5-m/description)

![Dashboard settings](https://github.com/blynkkk/blynk-server/blob/master/docs/overview/dash_settings.png)
![Widgets Box](https://github.com/blynkkk/blynk-server/blob/master/docs/overview/widgets_box.png)
![Dashboard](https://github.com/blynkkk/blynk-server/blob/master/docs/overview/dash.png)
![Dashboard2](https://github.com/blynkkk/blynk-server/blob/master/docs/overview/dash2.png)

# Содержание
- [Скачать](https://github.com/GeekHubMedia/GeekHub-Blynk-Server/blob/master/README.md#blynk-%D1%81%D0%B5%D1%80%D0%B2%D0%B5%D1%80)
- [Требования](https://github.com/GeekHubMedia/GeekHub-Blynk-Server/blob/master/README.md#%D0%A2%D1%80%D0%B5%D0%B1%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D1%8F)
- [Установка локального сервера](https://github.com/GeekHubMedia/GeekHub-Blynk-Server/blob/master/README.md#%D0%91%D1%8B%D1%81%D1%82%D1%80%D0%B0%D1%8F-%D0%BD%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B0-%D0%BB%D0%BE%D0%BA%D0%B0%D0%BB%D1%8C%D0%BD%D0%BE%D0%B3%D0%BE-%D1%81%D0%B5%D1%80%D0%B2%D0%B5%D1%80%D0%B0)
- [Установка локального сервера на Raspberry Pi](https://github.com/GeekHubMedia/GeekHub-Blynk-Server/blob/master/README.md#%D0%91%D1%8B%D1%81%D1%82%D1%80%D0%B0%D1%8F-%D0%BD%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B0-%D0%BB%D0%BE%D0%BA%D0%B0%D0%BB%D1%8C%D0%BD%D0%BE%D0%B3%D0%BE-%D1%81%D0%B5%D1%80%D0%B2%D0%B5%D1%80%D0%B0-%D0%BD%D0%B0-raspberry-pi)
- [Настройка авто перезагрузки сервера на системах Unix(Linux)](https://github.com/GeekHubMedia/GeekHub-Blynk-Server/blob/master/README.md#%D0%92%D0%BA%D0%BB%D1%8E%D1%87%D0%B5%D0%BD%D0%B8%D0%B5-%D0%B0%D0%B2%D1%82%D0%BE%D0%BC%D0%B0%D1%82%D0%B8%D1%87%D0%B5%D1%81%D0%BA%D0%BE%D0%B3%D0%BE-%D0%BF%D0%B5%D1%80%D0%B5%D0%B7%D0%B0%D0%BF%D1%83%D1%81%D0%BA%D0%B0-%D1%81%D0%B5%D1%80%D0%B2%D0%B5%D1%80%D0%B0-%D0%B2-unix-%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D0%B0%D1%85)
- [Настройка авто перезагрузки сервера на Windows](https://github.com/GeekHubMedia/GeekHub-Blynk-Server/blob/master/README.md#%D0%92%D0%BA%D0%BB%D1%8E%D1%87%D0%B5%D0%BD%D0%B8%D0%B5-%D0%B0%D0%B2%D1%82%D0%BE%D0%BC%D0%B0%D1%82%D0%B8%D1%87%D0%B5%D1%81%D0%BA%D0%BE%D0%B3%D0%BE-%D0%BF%D0%B5%D1%80%D0%B5%D0%B7%D0%B0%D0%BF%D1%83%D1%81%D0%BA%D0%B0-%D1%81%D0%B5%D1%80%D0%B2%D0%B5%D1%80%D0%B0-%D0%B2-windows)
- [Инструкция по обновлению для Unix (Linux) Систем](https://github.com/GeekHubMedia/GeekHub-Blynk-Server/blob/master/README.md#%D0%98%D0%BD%D1%81%D1%82%D1%80%D1%83%D0%BA%D1%86%D0%B8%D1%8F-%D0%BF%D0%BE-%D0%BE%D0%B1%D0%BD%D0%BE%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D1%8E-%D0%B4%D0%BB%D1%8F-unix---%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC)
- [Инструкция по обновлению для Windows](https://github.com/GeekHubMedia/GeekHub-Blynk-Server/blob/master/README.md#%D0%98%D0%BD%D1%81%D1%82%D1%80%D1%83%D0%BA%D1%86%D0%B8%D1%8E-%D0%BF%D0%BE-%D0%BE%D0%B1%D0%BD%D0%BE%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D1%8E-%D0%B4%D0%BB%D1%8F-windows)
- [Подключения Blynk к локальному серверу](https://github.com/GeekHubMedia/GeekHub-Blynk-Server/blob/master/README.md#%D0%98%D0%B7%D0%BC%D0%B5%D0%BD%D0%B5%D0%BD%D0%B8%D1%8F-%D0%B2-%D0%BF%D1%80%D0%B8%D0%BB%D0%BE%D0%B6%D0%B5%D0%BD%D0%B8%D0%B5-%D0%B8-%D1%8D%D1%81%D0%BA%D0%B8%D0%B7%D0%B5)
- [Расширенная настройка локального сервера](https://github.com/GeekHubMedia/GeekHub-Blynk-Server/blob/master/README.md#%D0%A0%D0%B0%D1%81%D1%88%D0%B8%D1%80%D0%B5%D0%BD%D0%BD%D0%B0%D1%8F-%D0%BD%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B0-%D0%BB%D0%BE%D0%BA%D0%B0%D0%BB%D1%8C%D0%BD%D0%BE%D0%B3%D0%BE-%D1%81%D0%B5%D1%80%D0%B2%D0%B5%D1%80%D0%B0)
- [Панель администратора](https://github.com/GeekHubMedia/GeekHub-Blynk-Server/blob/master/README.md#%D0%9F%D0%B0%D0%BD%D0%B5%D0%BB%D1%8C-%D0%B0%D0%B4%D0%BC%D0%B8%D0%BD%D0%B8%D1%81%D1%82%D1%80%D0%B0%D1%82%D0%BE%D1%80%D0%B0)
- [HTTP/S RESTful API](https://github.com/GeekHubMedia/GeekHub-Blynk-Server/blob/master/README.md#http--s-restful)
- [Включение почты на локальном сервервере](https://github.com/GeekHubMedia/GeekHub-Blynk-Server/blob/master/README.md#%D0%92%D0%BA%D0%BB%D1%8E%D1%87%D0%B5%D0%BD%D0%B8%D0%B5-%D0%BF%D0%BE%D1%87%D1%82%D1%8B-%D0%BD%D0%B0-%D0%BB%D0%BE%D0%BA%D0%B0%D0%BB%D1%8C%D0%BD%D0%BE%D0%BC-%D1%81%D0%B5%D1%80%D0%B2%D0%B5%D1%80%D0%B5)
- [Включение SMS на локальном сервере](https://github.com/GeekHubMedia/GeekHub-Blynk-Server/blob/master/README.md#%D0%92%D0%BA%D0%BB%D1%8E%D1%87%D0%B5%D0%BD%D0%B8%D0%B5-%D1%81%D0%BC%D1%81-%D0%BD%D0%B0-%D0%BB%D0%BE%D0%BA%D0%B0%D0%BB%D1%8C%D0%BD%D0%BE%D0%BC-%D1%81%D0%B5%D1%80%D0%B2%D0%B5%D1%80%D0%B5)
- [Включение хранилища необработанных данных](https://github.com/GeekHubMedia/GeekHub-Blynk-Server/blob/master/README.md#%D0%92%D0%BA%D0%BB%D1%8E%D1%87%D0%B5%D0%BD%D0%B8%D0%B5-%D1%85%D1%80%D0%B0%D0%BD%D0%B8%D0%BB%D0%B8%D1%89%D0%B0-%D0%BD%D0%B5%D0%BE%D0%B1%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%D0%BD%D0%BD%D1%8B%D1%85-%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D1%85)
- [Автоматическое шифрование данных](https://github.com/GeekHubMedia/GeekHub-Blynk-Server/blob/master/README.md#%D0%90%D0%B2%D1%82%D0%BE%D0%BC%D0%B0%D1%82%D0%B8%D1%87%D0%B5%D1%81%D0%BA%D0%BE%D0%B5-%D1%81%D0%BE%D0%B7%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5-%D1%88%D0%B8%D1%84%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D1%8F-%D1%81%D0%B5%D1%80%D1%82%D0%B8%D1%84%D0%B8%D0%BA%D0%B0%D1%82%D0%BE%D0%B2)
- [Руководство шифрования SSL/TLS сертефикатов](https://github.com/GeekHubMedia/GeekHub-Blynk-Server/blob/master/README.md#%D0%A0%D1%83%D0%BA%D0%BE%D0%B2%D0%BE%D0%B4%D1%81%D1%82%D0%B2%D0%BE-%D1%88%D0%B8%D1%84%D1%80%D0%BE%D0%B2%D0%BA%D0%B8-%D1%81%D0%B5%D1%80%D1%82%D0%B8%D1%84%D0%B8%D0%BA%D0%B0%D1%82%D0%BE%D0%B2-ssl--tls)
- [Создание собственных сертификатов SSL](https://github.com/GeekHubMedia/GeekHub-Blynk-Server/blob/master/README.md#%D0%A1%D0%BE%D0%B7%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5-%D1%81%D0%BE%D0%B1%D1%81%D1%82%D0%B2%D0%B5%D0%BD%D0%BD%D1%8B%D1%85-%D1%81%D0%B5%D1%80%D1%82%D0%B8%D1%84%D0%B8%D0%BA%D0%B0%D1%82%D0%BE%D0%B2-ssl)
- [Установка java для Ubuntu](https://github.com/GeekHubMedia/GeekHub-Blynk-Server/blob/master/README.md#%D0%A3%D1%81%D1%82%D0%B0%D0%BD%D0%BE%D0%B2%D0%B8%D1%82%D1%8C-java-%D0%B4%D0%BB%D1%8F-ubuntu)
- [Как работает Blynk?](https://github.com/GeekHubMedia/GeekHub-Blynk-Server/blob/master/README.md#%D0%9A%D0%B0%D0%BA-%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%D0%B5%D1%82-%D0%91%D0%BB%D0%B8%D0%BD%D0%BA)
- [Blynk протоколы](https://github.com/GeekHubMedia/GeekHub-Blynk-Server/blob/master/README.md#%D0%9F%D1%80%D0%BE%D1%82%D0%BE%D0%BA%D0%BE%D0%BB-%D0%91%D0%BB%D0%B8%D0%BD%D0%BA)

# НАЧНЕМ

## Blynk сервер
Сервер Blynk - это сервер Java с открытым исходным кодом [Netty](https://github.com/netty/netty), отвечающий за пересылку
данных между мобильным приложением Blynk и различными микроконтроллерами и SBC (например, Arduino, Raspberry Pi и т. д.).

**Скачать последнею версию сервера [здесь](https://github.com/blynkkk/blynk-server/releases).**

[![GitHub version](https://img.shields.io/github/release/blynkkk/blynk-server.svg)](https://github.com/blynkkk/blynk-server/releases/latest)
[![GitHub download](https://img.shields.io/github/downloads/blynkkk/blynk-server/total.svg)](https://github.com/blynkkk/blynk-server/releases/latest)
[![Build Status](https://travis-ci.org/blynkkk/blynk-server.svg?branch=master)](https://travis-ci.org/blynkkk/blynk-server)

## Требования
- Требуется Java 8/9 (OpenJDK, Oracle)
- Любая операционная система, которая имеет поддержку java
- Не менее 30 МБ ОЗУ (оперативной памяти) - (может быть меньше при настройке)
- Открытые порты 9443 (для приложения), 8442 (для аппаратного обеспечения без ssl), 8441 (для аппаратного обеспечения с ssl)

[Инструкция установки Java на Ubuntu](https://github.com/GeekHubMedia/GeekHub-Blynk-Server/blob/master/README.md#%D0%A3%D1%81%D1%82%D0%B0%D0%BD%D0%BE%D0%B2%D0%B8%D1%82%D1%8C-java-%D0%B4%D0%BB%D1%8F-ubuntu).

Для Windows загрузите Java [здесь](http://download.oracle.com/otn-pub/java/jdk/9+181/jre-9_windows-x64_bin.exe) и установите.

## Быстрая настройка локального сервера

+ Убедитесь, что вы используете Java 9

java -version
Output: java version "9"

+ Запустите сервер по умолчанию «аппаратный порт 8442» и по умолчанию «порт приложения 9443» (порт SSL)

java -jar server-0.31.0.jar -dataFolder /path

Вот и все!

**ПРИМЕЧАНИЕ: ```/ path``` должен быть реальным существующим путем в папку, где вы хотите хранить все свои данные **.

+ В конечном результате вы увидите такое сообщение:

Blynk Server successfully started.
All server output is stored in current folder in 'logs/blynk.log' file.

### Включение почты на локальном сервере
Чтобы включить уведомления по почте на локальном сервере, вам необходимо предоставить свои собственные учетные данные. Создайте файл ```mail.properties``` в той же папке, где``` server.jar```.
Свойства почты:

mail.smtp.auth=true
mail.smtp.starttls.enable=true
mail.smtp.host=smtp.gmail.com
mail.smtp.port=587
mail.smtp.username=YOUR_EMAIL_HERE
mail.smtp.password=YOUR_EMAIL_PASS_HERE

Пример настройки почты [здесь](https://github.com/blynkkk/blynk-server/blob/master/server/notifications/email/src/main/resources/mail.properties).

**ПРЕДУПРЕЖДЕНИЕ: разрешены только учетные записи gmail.**

**ПРИМЕЧАНИЕ.** Вам нужно настроить Gmail для работы с ненадежными приложениями.
Нажмите [здесь](https://www.google.com/settings/security/lesssecureapps), а затем нажмите «Ненадежные приложения заблокированы ».

## Быстрая настройка локального сервера на Raspberry Pi

+ Подключить Raspberry Pi через ssh;
+ Установить java 8:

sudo apt-get install oracle-java8-jdk

+ Убедитесь, что вы используете именно Java 8

java -version
Output: java version "1.8"

+ Загрузите Blynk сервер Jar файл (или вручную скопируйте его в Raspberry Pi через команду ssh и scp):

wget "https://github.com/blynkkk/blynk-server/releases/download/v0.31.0/server-0.31.0-java8.jar"

+ Запустите сервер по умолчанию «аппаратный порт 8442» и по умолчанию «порт приложения 9443» (порт SSL)

java -jar server-0.31.0-java8.jar -dataFolder /home/pi/Blynk 

Вот и все!

В конечном результате вы увидите следующее сообщение: 

Blynk Server successfully started.
All server output is stored in current folder in 'logs/blynk.log' file.

## Включение автоматического перезапуска сервера в UNIX-системах

+ Чтобы включить автоматический перезапуск сервера, найдите файл /etc/rc.local и добавьте:

java -jar /home/pi/server-0.31.0.jar -dataFolder /home/pi/Blynk &

+ Или если описанный выше подход не работает, выполните:

crontab -e

добавьте следующую строку:

@reboot java -jar /home/pi/server-0.31.0.jar -dataFolder /home/pi/Blynk &

Сохранить и выйти.

## Включение автоматического перезапуска сервера в Windows

+ Создать .bat файл:

start-blynk.bat

+ Вставьте в файл одну строку:

java -jar server-0.31.0.jar -dataFolder /home/pi/Blynk

+ Добавить файл bat в папку автозагрузки Windows

Вы также можете использовать этот [скрипт](https://github.com/blynkkk/blynk-server/tree/master/scripts/win) для запуска сервера.

## Инструкция по обновлению для unix - систем

**ВАЖНО**
Сервер должен всегда обновляться до того, как вы обновите приложение Blynk. Чтобы обновить сервер до более новой версии, вам нужно будет убить старый процесс и запустить новый.

+ Найти идентификатор процесса сервера Blynk

ps -aux | grep java

+ Вы должны увидеть что-то подобное:

username   10539  1.0 12.1 3325808 428948 pts/76 Sl   Jan22   9:11 java -jar server-0.31.0.jar   

+ Убить старый процесс

kill 10539

10539 - идентификатор процесса сервера blynk из вывода команды выше.

+ Запустить новый сервер [как обычно](https://github.com/GeekHubMedia/GeekHub-Blynk-Server/blob/master/README.md#%D0%91%D1%8B%D1%81%D1%82%D1%80%D0%B0%D1%8F-%D0%BD%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B0-%D0%BB%D0%BE%D0%BA%D0%B0%D0%BB%D1%8C%D0%BD%D0%BE%D0%B3%D0%BE-%D1%81%D0%B5%D1%80%D0%B2%D0%B5%D1%80%D0%B0-%D0%BD%D0%B0-raspberry-pi)

После этого вы можете обновить приложение Blynk. Понижение версии сервера не поддерживается.

**ВНИМАНИЕ!**
** ** не переустанавливайте сервер на более низкие версии. Вы можете потерять все свои данные.

## Инструкцию по обновлению для Windows

+ Открыть диспетчер задач;

+ Найти Java-процесс;

+ Остановить процесс;

+ Запустить новый сервер [как обычно](https://github.com/GeekHubMedia/GeekHub-Blynk-Server#%D0%91%D1%8B%D1%81%D1%82%D1%80%D0%B0%D1%8F-%D0%BD%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B0-%D0%BB%D0%BE%D0%BA%D0%B0%D0%BB%D1%8C%D0%BD%D0%BE%D0%B3%D0%BE-%D1%81%D0%B5%D1%80%D0%B2%D0%B5%D1%80%D0%B0-%D0%BD%D0%B0-raspberry-pi)

## Изменения в приложение и эскизе

+ Укажите настраиваемый путь к серверу в приложении

![Custom server icon](https://github.com/blynkkk/blynk-server/blob/master/docs/login.png)
![Server properties menu](https://github.com/blynkkk/blynk-server/blob/master/docs/custom.png)

+ Изменить тип вашего проводного подключения к интернету с

    ```
    Blynk.begin(auth);
    ```
    
    на
    
    ```
    Blynk.begin(auth, "your_host");
    ```
    
    или на
    
    ```
    Blynk.begin(auth, IPAddress(xxx,xxx,xxx,xxx));
    ```

+ Измените ваше WiFi подключения с
    
    ```        
    Blynk.begin(auth, SSID, pass));
    ```
   
    на
    
    ```
    Blynk.begin(auth, SSID, pass, "your_host");
    ```
    
    или на
    
    ```
    Blynk.begin(auth, SSID, pass, IPAddress(XXX,XXX,XXX,XXX));
    ```
+ Изменить ваш Raspberry Pi Javascript c
    ```
    var blynk = new Blynk.Blynk(AUTH, options = {connector : new Blynk.TcpClient()});
    ```
    
    на
    
    ```
    var blynk = new Blynk.Blynk(AUTH, options= {addr:"xxx.xxx.xxx.xxx"});
    ```
+ или в случае USB при запуске blynk-ser.sh предоставить опцию «-s» с адресом вашего локального сервера

./blynk-ser.sh -s you_host_or_IP

**ВАЖНО**
Блинк постоянно развивается. Мобильные приложения и сервер часто обновляются. Чтобы избежать проблем во время обновлений, отключите автоматическое обновление для приложения Blynk или одновременно обновите локальный сервер и приложение blynk, чтобы избежать возможных проблем с миграцией.

**ВАЖНО**
Локальный сервер Blynk отличается от сервера Blynk Cloud. Они не связаны вообще. Вы должны создать новую учетную запись при использовании локального сервера Blynk.

## Расширенная настройка локального сервера
Для большей гибкости вы можете расширить сервер с большим количеством опций, создав файл ```server.properties``` в той же папке, что и```server.jar```.
Пример можно найти [здесь](https://github.com/blynkkk/blynk-server/blob/master/server/core/src/main/resources/server.properties).
Вы также можете указать любой путь к файлу ```server.properties``` через аргумент командной строки``` -serverConfig```. Вы можете
делать то же самое с ```mail.properties``` через ``` -mailConfig``` и ```sms.properties``` через``` -smsConfig```.

Например:

java -jar server-0.31.0.jar -dataFolder /home/pi/Blynk -serverConfig /home/pi/someFolder/server.properties

Доступные параметры сервера:

+ Приложение Blynk, https, websockets, порт администратора

https.port=9443

+ Аппаратный простой порт tcp/ip

hardware.default.port=8442

+ Аппаратный порт ssl/tls (для аппаратного обеспечения, поддерживающего сокеты SSL/TLS)

hardware.ssl.port=8441

+ Для простоты Blynk уже предоставляет серверную банку со встроенными сертификатами SSL, поэтому у вас есть рабочий сервер из коробки через SSL / TLS-сокеты. Но поскольку сертификат и его частный ключ находятся на публике, это совершенно небезопасно. Поэтому, чтобы исправить это, вам нужно предоставить свои собственные сертификаты. И измените ниже свойства с указанием пути к вашему сертификату. и закрытый ключ, и это пароль. Узнайте, как создавать самозаверяющие сертификаты [здесь](# generate-ssl-certificate)

# Указывает на cert и ключ, который помещается в ту же папку, что и jar.

server.ssl.cert=./server_embedded.crt
server.ssl.key=./server_embedded.pem
server.ssl.key.pass=pupkin123

+ Порт Http и веб-сокетов

http.port=8080

+ Папка профилей пользователей. Папка, в которой будут сохраняться все профили пользователей. По умолчанию используется System.getProperty («java.io.tmpdir») / blynk. Будет создано, если не существует

data.folder=/tmp/blynk

+ Папка для всех журналов приложений. Будет создана, если оно не существует. «.» Это директория, из которого вы запускаете скрипт.

logs.folder=./logs

+ Уровень отладки журнала. Возможные значения: trace | debug | info | error. Определяет, насколько точным будет запись. Слева направо -> максимальная регистрация до минимума

log.level=trace

+ Максимально допустимое количество панелей пользователей.

user.dashboard.max.limit=100

+ 100-кратное ограничение скорости на пользователя. Вы также можете расширить этот предел на странице [hardware side](https://github.com/blynkkk/blynk-library/blob/f4e132652906d63d683abeed89f5d6ebe369e37a/Blynk/BlynkConfig.h#L42).

user.message.quota.limit=100

+ этот параметр определяет, как часто вы можете отправлять почту / твит / push или любое другое уведомление. Указано в секундах

notifications.frequency.user.quota.limit=60

+ Максимально разрешенный размер профиля пользователя. В Кб.

user.profile.max.size=128

+ Количество строк для хранения в терминальном виджете (данные истории терминала)

terminal.strings.pool.size=25

+ Максимально допустимое количество очереди уведомлений. Очередь, ответственная за обработку электронной почты, нажатие, отправка твитов. Из-за проблемы с производительностью - эта очередь обрабатывается в отдельном потоке, это требуется из-за блокировки характера всех вышеперечисленных операций. Обычно ограничение не должно быть достигнуто

notifications.queue.limit=5000

+ Количество потоков для выполнения операций блокировки - push, twits, emails, db query. Рекомендуется удерживать это значение до минимума, если вам не нужно выполнять много операций блокировки.

blocking.processor.thread.pool.limit=6

+ Период для очистки всей пользовательской БД на диск. В миллисекундах

profile.save.worker.period=60000

+ Указывает максимальный период времени, когда аппаратный сокет может быть бездействующим. После чего сокет будет закрыт из-за неактивности. Через несколько секунд. Оставьте его пустым для тайм-аута бесконечности

hard.socket.idle.timeout=15

+ В основном требуется настройка локальных серверов в случае, если пользователь хочет записывать необработанные данные в формате CSV. Дополнительную информацию см. В разделе [raw data](#raw-data-storage).

enable.raw.data.store=true

+ Адрес для открытия страницы администрирования. Необходимо начинать с "/". Для «/ admin» URL-адрес будет выглядеть так: «https://127.0.0.1:9443/admin».

admin.rootPath=/admin

+ Список IP-адресов администратора, разделенных запятыми. Разрешить доступ к пользовательскому интерфейсу администратора только для этих IP-адресов. Вы можете установить его для 0.0.0.0/0, чтобы разрешить доступ для всех. Вы можете использовать нотацию CIDR. Например, 192.168.0.53/24.

 allowed.administrator.ips=0.0.0.0/0

+ Имя и пароль администратора по умолчанию. Будет создан при запуске начального сервера

admin.email=admin@blynk.cc
admin.pass=admin

+ Хост для перенаправления пароля и генерации сертификата. По умолчанию текущий IP-адрес сервера взят из сетевого интерфейса «eth». Может быть заменено более дружественным именем хоста. Рекомендуется переопределить это свойство с помощью IP-адреса вашего сервера, чтобы избежать возможных проблем с решением узла.

server.host=blynk-cloud.com

+ Электронная почта, используемая для регистрации сертификата, может быть опущена, если вы уже указали ее в mail.properties.

contact.email=pupkin@gmail.com

+ Список пользователей с запятыми, которым разрешено создавать учетные записи. Оставьте его пустым, если не требуется никаких ограничений.

allowed.users.list=allowed1@gmail.com,allowed2@gmail.com

## Панель администратора

Сервер Blynk предоставляет панель администрирования, где вы можете контролировать свой сервер. Она доступна по этому URL-адресу:

https://your_ip:9443/admin

![Administration UI](https://github.com/blynkkk/blynk-server/blob/master/docs/admin_panel.png)

**ПРЕДУПРЕЖДЕНИЕ**
Пожалуйста, измените пароль администратора и его имя сразу после входа на страницу администратора. ** ЭТО МЕРЫ БЕЗОПАСНОСТИ **.

**ПРЕДУПРЕЖДЕНИЕ**
По умолчанию параметр ```allowed.administrator.ips``` разрешает доступ для всех. Другими словами,
доступной с любого другого компьютера. Ограничьте доступ к нему через свойство ```allowed.administrator.ips```.

### Отключение chrome https warning на localhost

- Вставить в адресную строку chrome 

 chrome://flags/#allow-insecure-localhost

- Вы должны увидеть выделенный текст, говорящий: «Разрешить недопустимые сертификаты для ресурсов, загруженных с localhost». Нажмите «Включить»

## HTTP / S RESTful
Blynk HTTP / S RESTful API позволяет легко считывать и записывать значения в / из Pins в приложениях и оборудовании Blynk.
Описание API Http можно найти [здесь](http://docs.blynkapi.apiary.io).

### Включение смс на локальном сервере
Чтобы включить уведомления SMS на локальном сервере, вам необходимо предоставить учетные данные для шлюза SMS (в настоящее время сервер Blynk
поддерживает только 1 провайдера - [Nexmo](https://www.nexmo.com/). Вам нужно создать файл ```sms.properties```
в той же папке, где находится server.jar.

nexmo.api.key=
nexmo.api.secret=

И заполните вышеуказанные свойства учетными данными, которые вы получите от Nexmo. (Учетная запись -> Настройки -> Настройки API).
Вы также можете отправлять SMS по электронной почте, если ваш оператор сотовой сети поддерживает это. См. [Обсуждение](http://community.blynk.cc/t/sms-notification-for-important-alert/2542) для более подробной информации.

## Включение хранилища необработанных данных
По умолчанию необработанное хранилище данных отключено (поскольку он много занимает место на диске).
Когда вы включаете его, каждая команда ```Blynk.virtualWrite``` будет сохранена в DB.
Вам необходимо будет установить PostgreSQL Database (** минимальная требуемая версия - 9.5 **), чтобы включить эту функцию:

#### 1. Включение необработанных данных на сервере

Включить необработанные данные в ```server.properties```:

enable.db=true
enable.raw.db.data.store=true

#### 2. Установите PostgreSQL. Вариант A

sudo sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt/ `lsb_release -cs`-pgdg main" >> /etc/apt/sources.list.d/pgdg.list'
wget -q https://www.postgresql.org/media/keys/ACCC4CF8.asc -O - | sudo apt-key add -
        
sudo apt-get update
sudo apt-get install postgresql postgresql-contrib

#### 2. Установите PostgreSQL. Вариант Б

sudo apt-get update
apt-get --no-install-recommends install postgresql-9.6 postgresql-contrib-9.6

#### 3. Скачать Blynk DB скрипт

wget https://raw.githubusercontent.com/blynkkk/blynk-server/master/server/core/src/main/resources/create_schema.sql

#### 4. Переместите файл create_schema.sql в папку temp (чтобы избежать проблем с разрешением)

mv create_schema.sql /tmp

Результат:

/tmp/create_schema.sql

Скопируйте его в буфер обмена с консоли.

#### 5. Подключитесь к PostgreSQL

sudo su - postgres
psql

#### 6. Создать Blynk DB, проверить пользователя и таблицы

 \i /tmp/create_schema.sql

```/ tmp / create_schema.sql``` - путь от шага 4.

Вы должны увидеть следующий вывод:

 postgres=# \i /tmp/create_schema.sql
        CREATE DATABASE
        You are now connected to database "blynk" as user "postgres".
        CREATE TABLE
        CREATE TABLE
        CREATE TABLE
        CREATE TABLE
        CREATE TABLE
        CREATE TABLE
        CREATE TABLE
        CREATE TABLE
        CREATE TABLE
        CREATE TABLE
        CREATE TABLE
        CREATE ROLE
        GRANT
        GRANT

#### Выход

\q
               
Теперь запустите свой сервер, и вы увидите следующий текст в файле ``` postgres.log```:

2017-03-02 16:17:18.367 - DB url : jdbc:postgresql://localhost:5432/blynk?tcpKeepAlive=true&socketTimeout=150
2017-03-02 16:17:18.367 - DB user : test
2017-03-02 16:17:18.367 - Connecting to DB...
2017-03-02 16:17:18.455 - Connected to database successfully.

ПРЕДУПРЕЖДЕНИЕ:
Исходные данные могут очень быстро сократить пространство на диске!

### Формат данных CSV

Формат данных:

значение, метка времени, DeviceId

Например:

10,1438022081332,0

Где ```10``` - значение булавки.
```1438022081332``` - разница, измеренная в миллисекундах, между текущим временем и полночью, 1 января 1970 г. UTC.
Чтобы отобразить дату / время в excel, вы можете использовать формулу:

= ((Column / (60 * 60 * 24) / 1000 + 25569))

```0``` - идентификатор устройства

### Автоматическое создание шифрования сертификатов

У последнего сервера Blynk есть супер классная функция - автоматическая генерация сертификатов Encrypt.
Однако он имеет несколько требований:

+ Добавить свойство ```server.host``` в файл``` server.properties```.
Например :

server.host = myhost.com

IP не поддерживается, это ограничение Let's Encrypt. Также имейте в виду, что ```myhost.com```
должны быть разрешены публичными DNS-серверами.

+ Добавить свойство ```contact.email``` в``` server.properties```. Например :

contact.email=test@gmail.com

+ Вам нужно запустить сервер на порту 80 (требуется root или права администратора) или
сделать [переадресацию портов](# port-forwarding-for-https-api) на порт HTTP Blynk по умолчанию - 8080.

Это оно! Запускать сервер как обычный, а сертификаты будут генерироваться автоматически.

![](https://gifyu.com/images/certs.gif)

### Руководство шифровки сертификатов SSL / TLS

+ Сначала установите [certbot](https://github.com/certbot/certbot) на свой сервер (машина, на которой вы собираетесь запускать сервер Blynk)

wget https://dl.eff.org/certbot-auto
chmod a + x certbot-auto

+ Генерирование и проверка сертификатов (ваш сервер должен быть подключен к Интернету и иметь открытые порты 80/443)

./certbot-auto certonly --agree-tos --email YOUR_EMAIL --standalone -d YOUR_HOST

Например

./certbot-auto certonly --agree-tos --email pupkin@blynk.cc --standalone -d blynk.cc

+ Затем добавьте файл ```server.properties``` (в папку с server.jar)

server.ssl.cert = / и т.д. / letsencrypt / живой / YOUR_HOST / fullchain.pem
server.ssl.key = / и т.д. / letsencrypt / живой / YOUR_HOST / privkey.pem
server.ssl.key.pass =

### Создание собственных сертификатов SSL

+ Создать самозаверяющий сертификат и ключ

openssl req -x509 -nodes -days 1825 -newkey rsa: 2048 -keyout server.key -out server.crt

+ Преобразование server.key в файл закрытого ключа PKCS # 8 в формате PEM

openssl pkcs8 -topk8 -inform PEM -outform PEM -in server.key -out server.pem

Если вы подключаете аппаратное обеспечение с помощью [USB-скрипта](https://github.com/blynkkk/blynk-library/tree/master/scripts), вы должны указать опцию '-s', указывающую на «общее имя» (имя хоста), вы указанных во время создания сертификата.

В качестве вывода вы получите файлы server.crt и server.pem, которые необходимо предоставить для свойств server.ssl.

### Установить java для Ubuntu

sudo apt-add-repository ppa:webupd8team/java
sudo apt-get update
sudo apt-get install oracle-java9-installer
        
или 

sudo apt-get install oracle-java8-installer

в случае, если в вашей системе еще нет Java 9.

### Перенаправление портов для API HTTP / S

sudo iptables -t nat -A PREROUTING -p tcp --dport 80 -j REDIRECT - to-port 8080
sudo iptables -t nat -A PREROUTING -p tcp --dport 443 -j REDIRECT - to-port 9443

### Включение генерации QR на сервере

sudo apt-get install libxrender1

### За маршрутизатором wifi
Если вы хотите запустить сервер Blynk за WiFi-маршрутизатором и хотите, чтобы он был доступен из Интернета, вам необходимо добавить правило переадресации портов на вашем маршрутизаторе. Это необходимо для перенаправления всех запросов, которые поступают на маршрутизатор в локальной сети на сервер Blynk.

### Как построить
Blynk имеет кучу интеграционных тестов, требующих DB, поэтому вам нужно пропустить тесты во время сборки.

mvn clean install -Dmaven.test.skip = true

### Как работает Блинк?
Когда аппаратное обеспечение подключается к облаку Blynk, оно открывает либо соединение ssl / tls keep-alive на порту 8441, либо в режиме keep-alive plain
tcp / ip на порту 8442. Приложение Blynk открывает взаимное соединение ssl / tls с Blynk Cloud на порту 443 (9443 для локальных серверов).
Blynk Cloud отвечает за пересылку сообщений между оборудованием и приложением. В обоих приложениях (приложениях и оборудовании) Blynk использует
собственный двоичный протокол, описанный ниже.

### Протокол Блинк

Blynk передает двоичные сообщения со следующей структурой:

| Команда         | Идентификатор сообщения | Длина / Статус   | Тело       |
|:---------------:|:-----------------------:|:----------------:|:----------:|
| 1 байт          | 2 байта                 | 2 байта          | Переменная |

Идентификатор сообщения и длина [big endian](http://en.wikipedia.org/wiki/Endianness#Bigendian).
Тело имеет формат, специфичный для команд.

Определения команд и состояний: [BlynkProtocolDefs.h](https://github.com/blynkkk/blynk-library/blob/master/Blynk/BlynkProtocolDefs.h)

Типичная библиотека Blynk знает, как отправить (S) / процесс (P):

S BLYNK_CMD_LOGIN + токен аутентификации
SP BLYNK_CMD_PING
SP BLYNK_CMD_RESPONSE
SP BLYNK_CMD_BRIDGE
SP BLYNK_CMD_HARDWARE
S BLYNK_CMD_TWEET
S BLYNK_CMD_EMAIL
S BLYNK_CMD_PUSH_NOTIFICATION

## Лицензирование
[Лицензия GNU GPL](https://github.com/blynkkk/blynk-server/blob/master/license.txt)
