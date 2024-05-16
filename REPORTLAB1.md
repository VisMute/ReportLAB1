## Лабораторная работа №1
## Студент
Кашкин Николай ИУ8-23
## Homework
1. Скачайте библиотеку *boost* с помощью утилиты **wget**. Адрес для скачивания 'https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz'.
```
$ wget https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz
```
Вывод:
```
--2024-03-27 18:31:35--  https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz
Распознаётся sourceforge.net (sourceforge.net)… 104.18.37.111, 172.64.150.145, 2606:4700:4400::6812:256f, ...
Подключение к sourceforge.net (sourceforge.net)|104.18.37.111|:443... соединение установлено.
HTTP-запрос отправлен. Ожидание ответа… 301 Moved Permanently
Адрес: https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz/ [переход]
--2024-03-27 18:31:35--  https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz/
Повторное использование соединения с sourceforge.net:443.
HTTP-запрос отправлен. Ожидание ответа… 301 Moved Permanently
Адрес: https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz/download [переход]
--2024-03-27 18:31:35--  https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz/download
Повторное использование соединения с sourceforge.net:443.
HTTP-запрос отправлен. Ожидание ответа… 302 Found
Адрес: https://downloads.sourceforge.net/project/boost/boost/1.69.0/boost_1_69_0.tar.gz?ts=gAAAAABmBDvYZOR1ab8xwfVcmjNL0I2r0TUnKC5paInR79YzT3IkzKB3AfVwQzQjs_YeWi4PI3zLZTINmg_NHh5iTdy1r9kr3w%3D%3D&use_mirror=deac-ams&r= [переход]
--2024-03-27 18:31:36--  https://downloads.sourceforge.net/project/boost/boost/1.69.0/boost_1_69_0.tar.gz?ts=gAAAAABmBDvYZOR1ab8xwfVcmjNL0I2r0TUnKC5paInR79YzT3IkzKB3AfVwQzQjs_YeWi4PI3zLZTINmg_NHh5iTdy1r9kr3w%3D%3D&use_mirror=deac-ams&r=
Распознаётся downloads.sourceforge.net (downloads.sourceforge.net)… 204.68.111.105
Подключение к downloads.sourceforge.net (downloads.sourceforge.net)|204.68.111.105|:443... соединение установлено.
HTTP-запрос отправлен. Ожидание ответа… 302 Found
Адрес: https://deac-ams.dl.sourceforge.net/project/boost/boost/1.69.0/boost_1_69_0.tar.gz [переход]
--2024-03-27 18:31:36--  https://deac-ams.dl.sourceforge.net/project/boost/boost/1.69.0/boost_1_69_0.tar.gz
Распознаётся deac-ams.dl.sourceforge.net (deac-ams.dl.sourceforge.net)… 185.34.27.55
Подключение к deac-ams.dl.sourceforge.net (deac-ams.dl.sourceforge.net)|185.34.27.55|:443... соединение установлено.
HTTP-запрос отправлен. Ожидание ответа… 200 OK
Длина: 111710205 (107M) [application/x-gzip]
Сохранение в: ‘boost_1_69_0.tar.gz’

boost_1_69_0.tar.gz                                100%[================================================================================================================>] 106,53M  4,57MB/s    за 34s     

2024-03-27 18:32:10 (3,16 MB/s) - ‘boost_1_69_0.tar.gz’ сохранён [111710205/111710205]
```
2. Разархивируйте скаченный файл в директорию ~/boost_1_69_0.
```
$ tar -xf boost_1_69_0.tar.gz -C ~/
```
Данная команда не выводить ничего в командную строку
3. Подсчитайте количество файлов в директории ~/boost_1_69_0 не включая вложенные директории.
```
$ find ~/boost_1_69_0 -maxdepth 1 -type f | wc -l
```
Вывод:
```
12
```
4. Подсчитайте количество файлов в директории ~/boost_1_69_0 включая вложенные директории.
```
$ find ~/boost_1_69_0 -type f | wc -l
```
Вывод:
```
61191
```
5. Подсчитайте количество заголовочных файлов, файлов с расширением .cpp, сколько остальных файлов (не заголовочных и не .cpp).
```
$ find ~/boost_1_69_0 -type f -iname "*.hpp" | wc -l
```
Вывод:
```
14912
```
```
$ find ~/boost_1_69_0 -type f -iname "*.cpp" | wc -l
```
Вывод:
```
13774
```
```
$ find ~/boost_1_69_0 -type f ! -name "*.hpp" ! -name "*.cpp" | wc -l
```
Вывод:
```
32505
```
6. Найдите полный путь до файла any.hpp внутри библиотеки boost.
```
$ find ~/boost_1_69_0 -type f -name "any.hpp"
```
Вывод:
```
/home/meguai/boost_1_69_0/boost/hana/any.hpp
/home/meguai/boost_1_69_0/boost/hana/fwd/any.hpp
/home/meguai/boost_1_69_0/boost/type_erasure/any.hpp
/home/meguai/boost_1_69_0/boost/spirit/home/support/algorithm/any.hpp
/home/meguai/boost_1_69_0/boost/proto/detail/any.hpp
/home/meguai/boost_1_69_0/boost/any.hpp
/home/meguai/boost_1_69_0/boost/fusion/include/any.hpp
/home/meguai/boost_1_69_0/boost/fusion/algorithm/query/any.hpp
/home/meguai/boost_1_69_0/boost/fusion/algorithm/query/detail/any.hpp
/home/meguai/boost_1_69_0/boost/xpressive/detail/utility/any.hpp
/home/meguai/boost_1_69_0/boost_output/include/boost/hana/any.hpp
/home/meguai/boost_1_69_0/boost_output/include/boost/hana/fwd/any.hpp
/home/meguai/boost_1_69_0/boost_output/include/boost/type_erasure/any.hpp
/home/meguai/boost_1_69_0/boost_output/include/boost/spirit/home/support/algorithm/any.hpp
/home/meguai/boost_1_69_0/boost_output/include/boost/proto/detail/any.hpp
/home/meguai/boost_1_69_0/boost_output/include/boost/any.hpp
/home/meguai/boost_1_69_0/boost_output/include/boost/fusion/include/any.hpp
/home/meguai/boost_1_69_0/boost_output/include/boost/fusion/algorithm/query/any.hpp
/home/meguai/boost_1_69_0/boost_output/include/boost/fusion/algorithm/query/detail/any.hpp
/home/meguai/boost_1_69_0/boost_output/include/boost/xpressive/detail/utility/any.hpp
```
7. Выведите в консоль все файлы, где упоминается последовательность boost::asio.
```
$ grep -r "boost::asio" ~/boost_1_69_0
$ grep -r "boost::asio" ~/boost_1_69_0 > ~/boost_1_69_0_files_with_boost_asio.txt
```
[Вывод в файле 1.txt](https://gist.github.com/VisMute/aae9a6458884c6d6a1ec3dec1e8ae79a)
8. Скомпилируйте boost.
```
$ sudo apt install libicu-dev
$ ./bootstrap.sh --prefix=boost_output
$ ./bootstrap.sh --prefix=boost_output --with-icu=
$ ./b2 install
```
[Вывод в файле 2.txt](https://gist.github.com/VisMute/a63293d5d40ac1cfe062999241129c4b) 
[Вывод в файле 3.txt](https://gist.github.com/VisMute/7a24c4c98d0f5c4f6345997eacc447e4)
[Вывод в файле 4.txt](https://gist.github.com/VisMute/931fdf37d1c6f167c67146d62aacb0aa)
[Вывод в файле 5.txt](https://gist.github.com/VisMute/354dc99acbd9d07733bd4f84920a0921)
9. Перенесите все скомпилированные на предыдущем шаге статические библиотеки в директорию ~/boost-libs.
```
$ mv boost_output/lib/*.a ~/boost-libs
```
10. Подсчитайте сколько занимает дискового пространства каждый файл в этой директории.
```
$ du -sh ~/boost-libs/*
```
Вывод:
```
4,0K	/home/meguai/boost-libs/libboost_atomic.a
236K	/home/meguai/boost-libs/libboost_chrono.a
148K	/home/meguai/boost-libs/libboost_container.a
24K	/home/meguai/boost-libs/libboost_context.a
344K	/home/meguai/boost-libs/libboost_contract.a
152K	/home/meguai/boost-libs/libboost_date_time.a
4,0K	/home/meguai/boost-libs/libboost_exception.a
240K	/home/meguai/boost-libs/libboost_fiber.a
416K	/home/meguai/boost-libs/libboost_filesystem.a
880K	/home/meguai/boost-libs/libboost_graph.a
172K	/home/meguai/boost-libs/libboost_iostreams.a
580K	/home/meguai/boost-libs/libboost_math_c99.a
488K	/home/meguai/boost-libs/libboost_math_c99f.a
504K	/home/meguai/boost-libs/libboost_math_c99l.a
2,8M	/home/meguai/boost-libs/libboost_math_tr1.a
2,8M	/home/meguai/boost-libs/libboost_math_tr1f.a
2,8M	/home/meguai/boost-libs/libboost_math_tr1l.a
216K	/home/meguai/boost-libs/libboost_prg_exec_monitor.a
1,6M	/home/meguai/boost-libs/libboost_program_options.a
84K	/home/meguai/boost-libs/libboost_random.a
3,1M	/home/meguai/boost-libs/libboost_regex.a
1,2M	/home/meguai/boost-libs/libboost_serialization.a
24K	/home/meguai/boost-libs/libboost_stacktrace_addr2line.a
24K	/home/meguai/boost-libs/libboost_stacktrace_backtrace.a
16K	/home/meguai/boost-libs/libboost_stacktrace_basic.a
4,0K	/home/meguai/boost-libs/libboost_stacktrace_noop.a
4,0K	/home/meguai/boost-libs/libboost_system.a
2,3M	/home/meguai/boost-libs/libboost_test_exec_monitor.a
56K	/home/meguai/boost-libs/libboost_timer.a
2,3M	/home/meguai/boost-libs/libboost_unit_test_framework.a
4,6M	/home/meguai/boost-libs/libboost_wave.a
780K	/home/meguai/boost-libs/libboost_wserialization.a
```
11. Найдите топ10 самых "тяжёлых".
```
$ find . -type f -exec du -h {} +|sort -rh | head -n 10
```
Вывод:
```
4,6M	./libboost_wave.a
3,1M	./libboost_regex.a
2,8M	./libboost_math_tr1l.a
2,8M	./libboost_math_tr1f.a
2,8M	./libboost_math_tr1.a
2,3M	./libboost_unit_test_framework.a
2,3M	./libboost_test_exec_monitor.a
1,6M	./libboost_program_options.a
1,2M	./libboost_serialization.a
880K	./libboost_graph.a
```
