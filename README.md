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
![](https://github.com/AlexandraPirog/Final-Task/blob/master/%D0%91%D0%BB%D0%BE%D0%BA-%D1%81%D1%85%D0%B5%D0%BC%D0%B0.png)

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

![](https://github.com/AlexandraPirog/Final-Task/blob/master/%D0%9A%D0%BE%D0%BC%D0%BC%D0%B8%D1%82%D1%8B.png)

## Скриншот решения 
![](https://github.com/AlexandraPirog/Final-Task/blob/master/%D0%A0%D0%B5%D1%88%D0%B5%D0%BD%D0%B8%D0%B5.png)
