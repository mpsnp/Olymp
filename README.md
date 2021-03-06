# Olymp

Репозиторий для олимпиадной подготовки студентов КубГУ

# Основные положения
* Для мультиплатформенности и компактности всего проекта в целом, в репозитории будем хранить только исходники, а для удобства разработки использовать мультиплатформенную систему сборки проектов [CMake](http://ru.wikipedia.org/wiki/CMake). 

* Так-же предлагается разработать свой [стандарт оформления кода](http://ru.wikipedia.org/wiki/%D0%A1%D1%82%D0%B0%D0%BD%D0%B4%D0%B0%D1%80%D1%82_%D0%BE%D1%84%D0%BE%D1%80%D0%BC%D0%BB%D0%B5%D0%BD%D0%B8%D1%8F_%D0%BA%D0%BE%D0%B4%D0%B0) (или позаимствовать), которого будут придерживаться **все** участники проекта, для облегчения читаемости, понимания и красоты кода (в идеале код должен читаться с листа, без комментариев).

* Работать в отдельной ветке, а в `master` сливать будем на встрече лучший из вариантов.

# Подготовка к работе (генерация проекта)
Кто уже знаком с использованием CMake, может смело пропускать данный этап.

## Подготовка дирректории для сборки.
Просто создаем папку с названием Build/build и переходим в нее. Почему с таким: просто она уже стандартно игнорится, да и понятно что там будет.

    mkdir Build
    cd Build

## Сборка проекта
Все просто: вызываем `cmake -G <Generator> ..` где `<Generator>` - нужный нам генератор проекта. Список генераторов можно посмотреть, вызвав `cmake` без параметров. Так-же, если вы под системой из семейства UNIX, то `-G <Generator>` можно опускать, тогда будет происходить генерация обычного `Makefile`. После чего открываем сгенерированный проект или компилируем. 

Под UNIX системой создание исполняемого файла будет выглядеть примерно так:

    cmake ..
    make

Приятной работы.