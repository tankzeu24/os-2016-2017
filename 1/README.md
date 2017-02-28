# Първа среща

## Инфо

Имейл:
* `rgeorgiev583 at gmail dot com`
* `radoslavg1 at uni-sofia dot bg`


## Какво ще учим

Основните команди и системни извиквания в Unix, в частност Linux.


### Разпределение

* ~70% Bash:  основните команди в Unix и основните програмни конструкции в Bash.
* ~30% C:  основните системни извиквания и прости примерни програми на C, в които те се използват.


## Подготовка на работната среда

### Логване на OS server

#### Как се случва

* от Windows: чрез *PuTTY*.
* от Unix-базирана ОС: чрез *ssh*.


#### *PuTTY*

* IP адрес (в полето **Host Name**): `10.0.2.17`
* Порт (в полето **Port**): `22`
* **Connection Type**: *SSH*


#### *SSH*

		$ ssh sXXXXX@10.0.2.17


След успешно свързване със сървъра, трябва да се логнете със следните данни:

* Потребителско име (*username*): `sXXXXX` (където `XXXXX` е факултетният номер на студента)
* Парола: `student`


### Разлогване

* `logout`
* `exit`


### Вкъщи

Имате няколко варианта:

* VirtualBox - най-лесният вариант
* Инсталиране на Linux на *bare* хардуер - малко по-неприятно за начинаещи
* Vagrant - за любители на командния ред


## Файлове

В Unix всички съставни части на файловата система са файлове, включително директориите.


### Файлова йерархия

Всеки файл има име и други свързани с него метаданни.
Директориите съдържат файлове и други директории.
Те образуват кореново дърво по реда на влагането си една в друга.


### Метаданни за файловете

* Размер:  всеки файл има такъв.
* Разрешения:  три октални числа (четене/писане/изпълнение) съответно за потребител, групата му и всички останали.
* Собственик:  потребител и група, към която той принадлежи.


## Няколко команди

`pwd` - изкарва текущата директория
`echo` - извежда аргументите си
`date` - извежда текущата дата
`ls` - извежда информация за файловете в текущата папка
`cd` - променя текущата директория
`man` - извежда информация за въпросната команда


## Задачи

1. Изведете пътя към `make`:

		$ which make

2. Изведете файла `/etc/passwd`:

		$ cat /etc/passwd

3. Изведете няколко файла един след друг с една команда:

		$ cat file1 file2 file3 ...

4. Въведете нещо от стандартния вход във файл:

		$ cat > file

5. Създайте празен файл:

		$ > file
		$ echo /dev/null > file

6. Направете така, че дадена команда да не изведе нищо:

		$ команда > file

	Например:

		$ cat /dev/null > file

7. Изчистете терминала си:

		$ clear

8. Изведете списък с файловете в `/etc`, които започват с `p`:

		$ ls /etc/p*