# Итоговая проверочная работа (1 блок)

1.Создать репозиторий на GitHub

2.Нарисовать блок-схему алгоритма (можно обойтись блок-схемой основной содержательной части, если вы выделяете её в отдельный метод)

3.Снабдить репозиторий оформленным текстовым описанием решения (файл README.md)

4.Написать программу, решающую поставленную задачу

5.Использовать контроль версий в работе над этим небольшим проектом (не должно быть так, что всё залито одним коммитом, как минимум этапы 2, 3, и 4 должны быть расположены в разных коммитах)

**Задача**

Написать программу, которая из имеющегося массива строк формирует новый массив из строк, длина которых меньше, либо равна 3 символам. Первоначальный массив можно ввести с клавиатуры, либо задать на старте выполнения алгоритма. При решении не рекомендуется пользоваться коллекциями, лучше обойтись исключительно массивами.

**Примеры:**

[“Hello”, “2”, “world”, “:-)”] → [“2”, “:-)”]

[“1234”, “1567”, “-2”, “computer science”] → [“-2”]

[“Russia”, “Denmark”, “Kazan”] → []

----------------------------------------------------------------------------
## Блок-схема решения задачи
![](https://sun9-31.userapi.com/impg/5DcLCcREPMdyDa0iI1gEwv02xUp9i7F6NapdHg/81RNW37ygqE.jpg?size=882x716&quality=96&sign=8b74c823e4d197358232084b37967197&type=album)

## Описание решения задачи
Для начала я воспользовалась командой ввода данных в массив, вывела этот массив.
Далее проверила элементы массива на соответствие условию **"<= 3"** . Записала новый массив с соответствующими элементами.


## Программа решения задачи в C#

Console.Clear();

System.Console.WriteLine("Введите размер массива");

int size = Convert.ToInt32(Console.ReadLine());

string[] myArray = InputArray();

int lenArr = 0;

for (int i = 0; i <= myArray.Length - 1; i++)

{
   
    if (myArray[i].Length <= 3) lenArr++;
}

string[] newArr = new string[lenArr];

int count = 0;

for (int i = 0; i <= myArray.Length - 1; i++)

{
    if (myArray[i].Length <= 3)

    {
        newArr[count] = myArray[i];
        count++;
    }
}

string[] InputArray()

{
    string[] myArray;

    myArray = new string[size];

    for (int i = 0; i < myArray.Length; i++)

    {
        System.Console.WriteLine($"Введите значение элемента массива индекса {i}");

        myArray[i] = Console.ReadLine();

    }

    return myArray;
}

System.Console.WriteLine($"Введенный массив: {string.Join(" | ", myArray)}");

Console.Write($"Новый массив: {string.Join(" | ", newArr)}");

## Скриншоты коммитов

![](https://sun9-7.userapi.com/impg/omB4GFW8-CmOU33h6aAaM628XWtBcVm3UkpvLQ/ZtzMzWfdGXA.jpg?size=1920x1008&quality=96&sign=159acf0380f6f2525ce396412c42b554&type=album)

## Скриншот решения 
![](https://sun9-42.userapi.com/impg/02qvNoh2uq3HfnTvoBXCX6F0NpRD8ow-ytwhqA/wdqA7D7yEXs.jpg?size=1920x1008&quality=96&sign=9636a49d1c03c6b176bebafcbe26bcd4&type=album)
