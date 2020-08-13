Скачивает файлы в несколько потоков по ссылкам в указанную директорию, показывая общее затраченное время и среднюю скорость загрузки.
Если ссылки повторяются, то файл просто копируется с новым именем (без повторного скачивания).

Для работы необходимо скачать файл в Realises (Downloader.jar).

Создаем .bat файл, кладем его вместе с Downloader.jar и вставляем в него следующее:
java -jar Downloader.jar 7 "D:\to_download.txt" "D:\Downloads"

где:
7 - количество потоков;
"D:\to_download.txt" - путь к файлу, откуда будут браться ссылки;
"D:\Downloads" - куда загрузятся файлы (создастся автоматически).

Пример файла to_download.txt представлен в папке "/files";
Можно создать свой по следующему шаблону:
http://kremlin.ru/static/pdf/constitution.pdf ImportantDocument

где:
http://kremlin.ru/static/pdf/constitution.pdf - прямая ссылка на скачиваемый файл;
ImportantDocument - имя, под которым мы хотим сохранить файл (расширение добавится само).

На каждой строчке должна быть одна ссылка и одно имя файла, разделенные пробелом.

(проект создан в учебных целях и использовать его нет смысла, так как любой браузер делает то же самое в одно нажатие)