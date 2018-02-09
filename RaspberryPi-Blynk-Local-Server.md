**Быстрая настройка локального сервера на Raspberry Pi**

Подключить Raspberry Pi через ssh;

Установить java 8:

sudo apt-get install oracle-java8-jdk

Убедитесь, что вы используете именно Java 8

java -version Output: java version "1.8"

Загрузите Blynk сервер Jar файл (или вручную скопируйте его в Raspberry Pi через команду ssh и scp):

wget "https://github.com/blynkkk/blynk-server/releases/download/v0.31.0/server-0.31.0-java8.jar"

Запустите сервер по умолчанию «аппаратный порт 8442» и по умолчанию «порт приложения 9443» (порт SSL)

java -jar server-0.31.0-java8.jar -dataFolder /home/pi/Blynk

Вот и все!

В конечном результате вы увидите следующее сообщение:

Blynk Server successfully started. All server output is stored in current folder in 'logs/blynk.log' file.

**Включение автоматического перезапуска сервера в UNIX-системах**

Чтобы включить автоматический перезапуск сервера, найдите файл /etc/rc.local и добавьте:

java -jar /home/pi/server-0.31.0.jar -dataFolder /home/pi/Blynk &

Или если описанный выше подход не работает, выполните:
crontab -e

добавьте следующую строку:

@reboot java -jar /home/pi/server-0.31.0.jar -dataFolder /home/pi/Blynk &

Сохранить и выйти.
