# matrix@0.0.1

### Задание
Написать программу, выполняющую арифмитические операции над **динамическими** матрицами. Программа должна поддерживать следующие операции:
- `+` `// rows1 == rows2 && columns1 == columns2`
- `-` `// rows1 == rows2 && columns1 == columns2`
- `*` `// columns1 == rows2`
- `T` - транспонирование

### Входные данные
Во входных данных заданы строки, следующего формата:
```
<имя файла, содержащего размеры 1-ой матрицы и ее элементы> <бинарная операция> <имя файла, содержащего размеры 2-ой матрицы и ее элементы>
```
```
<имя файла, содержащего размеры матрицы и ее элементы> <унарная операция>
```
### Выходные данные
Результат арифмитической операции или строка, сведетельствующая о возникновении ошибки:
- `An error has occured while reading input data`

### Замечания
Для реализации программы, необходимо воспользоваться классом следующего вида:
```
class matrix_t {
  int ** data;
  unsigned int rows;
  unsigned int collumns;
  
  matrix_t add( matrix_t & other );
  matrix_t sub( matrix_t & other );
  matrix_t mul( matrix_t & other );
  matrix_t trans( matrix_t & other );

  std::ifstream & read( std::ifstream & stream );
  std::ofstream & write( std::ofstream & stream );
};
```

### Примеры
```
A.txt
3, 3
2 2 2
2 2 2
2 2 2
```
```
B.txt
3, 3
1 1 1
1 1 1
1 1 1
```
```
C.txt
3, 3
1 2 3
4 5 6
7 8 9
```
#### входные данные
```
A.txt + B.txt
```
#### выходные данные
```
3 3 3
3 3 3
3 3 3
```
#### входные данные
```
A.txt - B.txt
```
#### выходные данные
```
1 1 1
1 1 1
1 1 1
```
#### входные данные
```
A.txt * B.txt
```
#### выходные данные
```
6 6 6
6 6 6
6 6 6
```
#### входные данные
```
C.txt T
```
#### выходные данные
```
1 4 7
2 5 8
3 6 9
```

# matrix@0.0.2

- Форкнуть тестовый [проект](https://github.com/justcppdev/matrix_example) работы с матрицами 
- Реализовать методы класса `matrix_t`
- Написать тесты ко всем открытым методам класса `matrix_t`


# matrix@0.0.3

- Добавить поддержку исключений
- Написать тесты обработки исключений
