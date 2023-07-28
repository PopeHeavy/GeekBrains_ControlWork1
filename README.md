# GeekBrains_ControlWork1

Снабдить репозиторий оформленным текстовым описанием решения (файл README.md)

Непосредственно задача:

>Задача: Написать программу, которая из имеющегося массива строк формирует новый массив из строк, длина которых меньше, либо равна 3 символам.
Первоначальный массив можно ввести с клавиатуры, либо задать на старте выполнения алгоритма.
При решении не рекомендуется пользоваться коллекциями, лучше обойтись исключительно массивами.

### 1. Задаем массив

`String[] string_array1 = new String[10] {"Monday", "Tue", "Wed", "Thu", "Fri", "Saturday", "Sunday", "Pizza Day", "Cat", "Garbage Day"};`

### 2. Задаем новый массив, в который мы будем вкладывать необходимые значения

`string[] string_array2 = new string[string_array1.Length];`

### 3. Вводим счетчик для данного массива

`int counter = 0;`

### 4. Через For loop проверяем строки в заданном массиве на необходимое условие (длина меньше или равна 3 символам) в течении количества раз равном длине массива.
Если строка подходит под условие - заносим её в новый массив и так до тех пор пока не закончится проверка заданного массива

```
for (int i = 0; i < string_array1.Length; i++)
{   
    if (string_array1[i].Length < 4)
    {
        string_array2[counter++] = string_array1[i];
    }
}
```

### 5. Чтобы избежать излишних NULL значений в массиве, нужно поменять размер нового массива, до количества новых элементов

`Array.Resize(ref string_array2, counter);`

### 6. Выводим полученный массив, чтобы убедиться что все правильно

`Console.WriteLine(String.Join(" ", string_array2));`

## Код для программы

```
String[] string_array1 = new String[10] {"Monday", "Tue", "Wed", "Thu", "Fri", "Saturday", "Sunday", "Pizza Day", "Cat", "Garbage Day"};

string[] string_array2 = new string[string_array1.Length];
int counter = 0;
for (int i = 0; i < string_array1.Length; i++)
{   
    if (string_array1[i].Length < 4)
    {
        string_array2[counter++] = string_array1[i];
    }
}
Array.Resize(ref string_array2, counter);
Console.WriteLine(String.Join(" ", string_array2));
```

