# Архиватор Хаффмана


## Описание

Архиватор, сделанный по алгоритму кодирования Хаффмана, сжимает текстовые файлы. 
Архиватор вызывается из командной строки и записывает результат в изначально определённые файлы.

## Принцип работы

Программу можно запустить в двух режимах:
1. Сжатие данных. В результате сжатия будет создан файл `encoded.zip`. Запуск программы 
в этом режиме:
```shell
./prog -c filename
```
- `prog`: название программы;
- `filename`: путь к файлу, который необходимо сжать;

2. Разжатие данных. Принимает `.zip` файл, который создан после запска программы в **режиме № 1**. 
Запуск программы в этом режиме:
```shell
./prog -d encoded.zip
```

## Сборка программы
 
### Cmake
Допустим, папка с проектом называется `compressor`. Чтобы собрать проект с помощью **CMakeLists.txt** Вам нужно:
```shell
cd compressor && mkdir build && cd build && cmake .. && make
```

### Командная строка
Допустим, папка с проектом называется `compressor`. Чтобы собрать проект из командной строки, Вам нужно в командной строке перейти в папку с проектом. Если у Вас компилятор gcc, то пишем следующее:
```shell
cd compressor
gcc -c *.c
gcc -o proga *.o
proga
```
