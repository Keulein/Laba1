## Laboratory work I

Данная лабораторная работа посвещена изучению утилит для разработки проектов

## Tasks

- [ ] 1. Ознакомиться со ссылками учебного материала
- [ ] 2. Выполнить инструкцию учебного материала
- [ ] 3. Составить отчет и отправить ссылку личным сообщением в **Slack**

## Tutorial

```bash
$ export GITHUB_USERNAME=tin1ock                         # Создание переменной окружения GITHUB_USERNAME
$ export GIST_TOKEN=tinlock228    # Создание переменной окружения GIST_TOKEN
$ alias edit=gedit                                             # Создание альтернативной версии команды "gedit"
```

```ShellSession
$ mkdir -p ${GITHUB_USERNAME}/workspace                       # Создание папки /duchessacid/workspace
$ cd ${GITHUB_USERNAME}/workspace                             #  Переход в папку /duchessacid/workspace
$ pwd                                                         # Вывод текущего каталога
/home/acid/duchessacid/workspace
$ cd ..                                                       # Переход по каталогу на раздел выше
$ pwd                                                         # # Вывод текущего каталога
/home/acid/duchessacid
```ShellSession
$ mkdir -p workspace/tasks/                                   # Создание папки workspace/tasks/
$ mkdir -p workspace/projects/                                # Создание папки workspace/projects/
$ mkdir -p workspace/reports/                                 # Создание папки workspace/reports/
$ cd workspace                                                #  Переход в папку /duchessacid/workspace
```
```ShellSession
# Debian
$ wget https://nodejs.org/dist/v6.11.5/node-v6.11.5-linux-x64.tar.xz    # Скачиваем файл по указанной ссылке
$ tar -xf node-v6.11.5-linux-x64.tar.xz                                 # Распаковываем архив
$ rm -rf node-v6.11.5-linux-x64.tar.xz                                  # Удаление архива
$ mv node-v6.11.5-linux-x64 node                                        # Переименовывание папки с node js 

```ShellSession
$ ls node/bin                                         # Вывод файловой файлов в папке node/bin 
node  npm
$ echo ${PATH}                                        # Вывод на экран переменной PATH
/usr/local/sbin:/usr/local/bin:/usr/bin:/usr/bin/site_perl:/usr/bin/vendor_perl:/usr/bin/core_perl
$ export PATH=${PATH}:`pwd`/node/bin                  # Добавление в PATH папку с программой node js
$ echo ${PATH}                                        # Вывод на экран переменной PATH
/usr/local/sbin:/usr/local/bin:/usr/bin:/usr/bin/site_perl:/usr/bin/vendor_perl:/usr/bin/core_perl:
/home/acid/duchessacid/workspace/node/bin
$ mkdir scripts                       # Создание папки /duchessacid/workspace/scripts
$ cat > scripts/activate<<EOF         # Запись строки в файл /duchessacid/workspace/scripts/activate
export PATH=\${PATH}:`pwd`/node/bin
EOF
$ source scripts/activate                             # Выполнение скрипта

```ShellSession
$ npm install -g gistup                             # Установка пакета gistup в node js
$ ls node/bin                                       # Вывод файлов из /duchessacid/workspace/node/bin
gistup  gistup-open  gistup-rename  node  npm

```ShellSession
$ cat > ~/.gistup.json <<EOF                        # Запись строки в файл ~/.gistup.json
{
  "token": "${GIST_TOKEN}"
}
EOF
```

## Report

```ShellSession
$ export LAB_NUMBER=01
$ git clone https://github.com/tp-labs/lab${LAB_NUMBER} tasks/lab${LAB_NUMBER}
$ mkdir reports/lab${LAB_NUMBER}
$ cp tasks/lab${LAB_NUMBER}/README.md reports/lab${LAB_NUMBER}/REPORT.md
$ cd reports/lab${LAB_NUMBER}
$ edit REPORT.md
$ gistup -m "lab${LAB_NUMBER}" # enter: yes↵
```

## Links

### Unix commands

- [ar](https://en.wikipedia.org/wiki/Ar_(Unix))
- [cat](https://en.wikipedia.org/wiki/Cat_(Unix))
- [cd](https://en.wikipedia.org/wiki/Cd_(command))
- [cp](https://en.wikipedia.org/wiki/Cp_(Unix))
- [cut](https://en.wikipedia.org/wiki/Cut_(Unix))
- [echo](https://en.wikipedia.org/wiki/Echo_(command))
- [env](https://en.wikipedia.org/wiki/Env_(shell))
- [ex](https://en.wikipedia.org/wiki/Ex_(editor))
- [file](https://en.wikipedia.org/wiki/File_(command))
- [find](https://en.wikipedia.org/wiki/Find)
- [ls](https://en.wikipedia.org/wiki/Ls)
- [man](https://en.wikipedia.org/wiki/Man_page)
- [mkdir](https://en.wikipedia.org/wiki/Mkdir)
- [mv](https://en.wikipedia.org/wiki/Mv)
- [nm](https://en.wikipedia.org/wiki/Nm_(Unix))
- [ps](https://en.wikipedia.org/wiki/Ps_(Unix))
- [pwd](https://en.wikipedia.org/wiki/Pwd)
- [rm](https://en.wikipedia.org/wiki/Rm_(Unix))
- [sed](https://en.wikipedia.org/wiki/Sed)
- [touch](https://en.wikipedia.org/wiki/Touch_(Unix))

### Package Managers

- [apt](http://help.ubuntu.ru/wiki/apt) | [dnf](https://en.wikipedia.org/wiki/DNF_(software)) | [yum](https://fedoraproject.org/wiki/Yum/ru)
- [brew](https://brew.sh) | [linuxbrew](http://linuxbrew.sh)
- [npm](https://docs.npmjs.com)

### Software

- [curl](https://www.gitbook.com/book/bagder/everything-curl/details)
- [wget](https://www.gnu.org/software/wget/manual/wget.pdf)
- [clang](https://clang.llvm.org)
- [g++](https://gcc.gnu.org/onlinedocs/gcc-4.0.2/gcc/G_002b_002b-and-GCC.html)
- [make](https://en.wikipedia.org/wiki/Make_(software))
- [open](https://developer.apple.com/legacy/library/documentation/Darwin/Reference/ManPages/man1/open.1.html)
- [openssl](https://www.openssl.org)
- [nano](https://www.nano-editor.org)
- [tree](https://linux.die.net/man/1/tree)
- [vim](http://www.vim.org)

## Homework

1. Скачайте библиотеку *boost* с помощью утилиты **wget**. Адрес для скачивания `https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz`.
2. Разархивируйте скаченный файл в директорию `~/boost_1_69_0`
3. Подсчитайте количество файлов в директории `~/boost_1_69_0` **не включая** вложенные директории.
4. Подсчитайте количество файлов в директории `~/boost_1_69_0` **включая** вложенные директории.
5. Подсчитайте количество заголовочных файлов, файлов с расширением `.cpp`, сколько остальных файлов (не заголовочных и не `.cpp`).
6. Найдите полный пусть до файла `any.hpp` внутри библиотеки *boost*.
7. Выведите в консоль все файлы, где упоминается последовательность `boost::asio`.
8. Скомпилирутйе *boost*. Можно воспользоваться [инструкцией](https://www.boost.org/doc/libs/1_61_0/more/getting_started/unix-variants.html#or-build-custom-binaries) или [ссылкой](https://codeyarns.com/2017/01/24/how-to-build-boost-on-linux/).
9. Перенесите все скомпилированные на предыдущем шаге статические библиотеки в директорию `~/boost-libs`.
10. Подсчитайте сколько занимает дискового пространства каждый файл в этой директории.
11. Найдите *топ10* самых "тяжёлых".
