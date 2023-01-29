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
<img src="file:///C:/Users/pirog/Desktop/Geekbrains/Финальная работа/Final_Task_Dev/Блок-Схема.png" />

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

<img src="file:///C:/Users/pirog/Documents/ShareX/Screenshots/2023-01/Code_6xBrqfDFxq.png" />

## Скриншот решения 
<img src="file:///C:/Users/pirog/Documents/ShareX/Screenshots/2023-01/Code_eYKiP5fno2.png" />