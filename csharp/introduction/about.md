## Ծրագրավորման հիմունքներ C#-ում

### Ներածություն

C# (արտասանվում է "See Sharp") - համացանցային ծրագրավորման լեզու, որը մշակվել է Microsoft-ի կողմից որպես մաս .NET Framework-ի։ Այն համակցում է C++-ի ու Java-ի լավագույն հատկանիշները։

Այս դասում մենք կծանոթանանք C#-ի հիմնական հասկացություններին, կսովորենք ինչպես ստեղծել պարզ կոնսոլային ծրագիր։

### Նախապայմաններ

- Տեղադրված Visual Studio կամ որևէ այլ IDE (օրինակ՝ Visual Studio Code)։
- .NET SDK տեղադրված։

### Առաջին ծրագիր C#-ում

1. **Նոր նախագիծ ստեղծել**

   - Բացեք Visual Studio։
   - Ընտրեք "Create a new project"։
   - Ընտրեք "Console App (.NET Core)"։
   - Տվեք նախագծի անուն (օրինակ՝ "HelloWorld")։
   - Սեղմեք "Create"։

2. **Ծրագիրը գրելը**

Ստեղծված նախագիծում հիմնական ֆայլը կլինի `Program.cs`, որտեղ կարող եք գրել ձեր առաջին ծրագիրը։ Ստորև բերված է պարզ օրինակ.

```csharp
using System;

namespace HelloWorld
{
    class Program
    {
        static void Main(string[] args)
        {
            // Տպել ողջույնի հաղորդագրություն
            Console.WriteLine("Բարեւ, աշխարհ!");
        }
    }
}
```

### Ծրագրի բաղադրիչները

- `using System;` - ներմուծում ենք System անվան տարածքը, որտեղից օգտվում ենք Console դասից։
- `namespace HelloWorld` - ստեղծում ենք անվան տարածք `HelloWorld`, որը կօգնի կազմակերպել կոդը։
- `class Program` - սահմանում ենք հիմնական դասը, որը կպարունակի մեր ծրագիրը։
- `static void Main(string[] args)` - մուտքային կետը, որտեղից ծրագիրը սկսում է իր աշխատանքը։

### Մեկնաբանություններ

```csharp
// Սա մեկ տողանի մեկնաբանություն է

/*
Սա
բազմատող
մեկնաբանություն է
*/
```

### Փոփոխականներ և տվյալների տեսակներ

```csharp
using System;

namespace VariableExamples
{
    class Program
    {
        static void Main(string[] args)
        {
            // Տվյալների տարբեր տեսակներ
            int age = 25; // Թիվ (integer)
            double salary = 12345.67; // Կրկնակի ճշտությամբ տասնորդական թիվ (double)
            char grade = 'A'; // Նիշ (character)
            string name = "Ani"; // Տեքստ (string)
            bool isStudent = true; // Բուլյան (boolean)

            // Տպում ենք արժեքները
            Console.WriteLine("Տարիքը: " + age);
            Console.WriteLine("Աշխատավարձը: " + salary);
            Console.WriteLine("Գնահատականը: " + grade);
            Console.WriteLine("Անունը: " + name);
            Console.WriteLine("Ուսանո՞ղ է: " + isStudent);
        }
    }
}
```

### Օպերատորներ

```csharp
using System;

namespace Operators
{
    class Program
    {
        static void Main(string[] args)
        {
            int a = 10;
            int b = 5;

            // Հաշվարկային օպերատորներ
            Console.WriteLine("a + b = " + (a + b));
            Console.WriteLine("a - b = " + (a - b));
            Console.WriteLine("a * b = " + (a * b));
            Console.WriteLine("a / b = " + (a / b));
            Console.WriteLine("a % b = " + (a % b));

            // Համեմատական օպերատորներ
            Console.WriteLine("a == b: " + (a == b));
            Console.WriteLine("a != b: " + (a != b));
            Console.WriteLine("a > b: " + (a > b));
            Console.WriteLine("a < b: " + (a < b));
            Console.WriteLine("a >= b: " + (a >= b));
            Console.WriteLine("a <= b: " + (a <= b));

            // Լոգիկական օպերատորներ
            bool x = true;
            bool y = false;
            Console.WriteLine("x && y: " + (x && y));
            Console.WriteLine("x || y: " + (x || y));
            Console.WriteLine("!x: " + (!x));
        }
    }
}
```

### Պայմանական օպերատորներ

```csharp
using System;

namespace ConditionalStatements
{
    class Program
    {
        static void Main(string[] args)
        {
            int number = 10;

            if (number > 0)
            {
                Console.WriteLine("Թիվը դրական է");
            }
            else if (number < 0)
            {
                Console.WriteLine("Թիվը բացասական է");
            }
            else
            {
                Console.WriteLine("Թիվը զրո է");
            }

            // switch հայտարարություն
            char grade = 'A';

            switch (grade)
            {
                case 'A':
                    Console.WriteLine("Գերազանց");
                    break;
                case 'B':
                    Console.WriteLine("Լավ");
                    break;
                case 'C':
                    Console.WriteLine("Բավարար");
                    break;
                case 'D':
                    Console.WriteLine("Անբավարար");
                    break;
                default:
                    Console.WriteLine("Անհայտ գնահատական");
                    break;
            }
        }
    }
}
```
