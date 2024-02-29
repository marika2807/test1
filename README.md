Решение:

1  Создан репозиторий test1

2 Создана блок-схема 

![схема](https://github.com/marika2807/test1/assets/144375982/f31dbced-f008-4d55-b955-032242862056)


3 Создан файл README.md, в котором сейчас находитесь.

4 Написана программа в папке kod (использованы функция для ввода и вывода массива)

Размер массива задаем с помощью переменной типа int. Заполнение реализовано через цикл for.
Также используем команду break.

ListOfCommands();
string[] array = new string[] {};

string inputNum = ReadInput("Введите номер команды: ");
switch (inputNum)
{
    case "1":
        array = new string[] { "Hello", "2", "world", ":-)" };
        break;
    case "2":
        array = new string[] { "1234", "1567", "-2", "computer science" };
        break;
    case "3":
        array = new string[] { "Russia", "Denmark", "Kazan" };
        break;
    default:
        Console.WriteLine($"{inputNum} - Команда указана неверно!");
        break;
}


int lengNewArray = 0;
for (int i = 0; i <= array.Length - 1; i++)
{
    if (array[i].Length <= 3) lengNewArray++;
}

string[] newArray = new string[lengNewArray];
int a = 0;

for (int i = 0; i <= array.Length - 1; i++)
{
    if (array[i].Length <= 3)
    {
        newArray[a] = array[i];
        a++;
    }
}

PrintArray(array);
Console.Write("→ ");
PrintArray(newArray);

void ListOfCommands()    
{
    Console.WriteLine();
    Console.WriteLine("СПИСОК КОМАНД:");
    Console.WriteLine("1 – использовать массив: [“Hello”, “2”, “world”, “:-)”]");
    Console.WriteLine("2 – использовать массив: [“1234”, “1567”, “-2”, “computer science”]");
    Console.WriteLine("3 – использовать массив: [“Russia”, “Denmark”, “Kazan”]");
    Console.WriteLine();
}

string ReadInput(string msg)  
{
    Console.Write(msg);
    return Console.ReadLine();
}

void PrintArray(string[] array)  
{
    Console.Write("[ ");
    for (int i = 0; i < array.Length; i++)
    {
        Console.Write($"“{array[i]}”, ");
    }
    Console.Write("] ");
}

5 -  cделаны коммиты 
