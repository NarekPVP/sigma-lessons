## Մեթոդներ և ֆունկցիաներ C#-ում

### Ներածություն

Մեթոդները (կամ ֆունկցիաները) ծրագրի այն մասերն են, որոնք իրականացնում են որոշակի գործողություններ և կարող են կանչվել այլ մասերից: Դրանք օգնում են բաժանել կոդը ավելի փոքր, վերաօգտագործվող բլոկների, ինչը հեշտացնում է կոդի գրումը, թեստավորումը և սպասարկումը։

### Մեթոդների ստեղծում և կանչում

#### Մեթոդի կառուցվածքը

Մեթոդի հիմնական կառուցվածքը հետևյալն է.

```csharp
returnType MethodName(parameterList)
{
    // Մեթոդի մարմին
}
```

- `returnType` - տիպը, որը մեթոդը վերադարձնում է (օրինակ՝ `int`, `string`, `void` եթե մեթոդը ոչինչ չի վերադարձնում):
- `MethodName` - մեթոդի անունը:
- `parameterList` - պարամետրերի ցուցակը, որոնք մեթոդը ընդունում է (կարող է դատարկ լինել):
- `{}` - մեթոդի մարմինը, որտեղ գրվում է գործողությունների հաջորդականությունը:

#### Պարզ մեթոդի օրինակ

Ստորև բերված է պարզ օրինակ մեթոդի, որը տպում է ողջույնի հաղորդագրություն:

```csharp
using System;

namespace MethodExamples
{
    class Program
    {
        static void Main(string[] args)
        {
            SayHello();
        }

        static void SayHello()
        {
            Console.WriteLine("Բարև, աշխարհ!");
        }
    }
}
```

Այս օրինակում `SayHello` մեթոդը ոչինչ չի ընդունում և ոչինչ չի վերադարձնում (`void`):

#### Մեթոդներ պարամետրերով

Մեթոդները կարող են ընդունել մեկ կամ մի քանի պարամետրեր:

```csharp
using System;

namespace MethodExamples
{
    class Program
    {
        static void Main(string[] args)
        {
            Greet("Անի");
        }

        static void Greet(string name)
        {
            Console.WriteLine("Բարև, " + name + "!");
        }
    }
}
```

Այս օրինակում `Greet` մեթոդը ընդունում է մեկ պարամետր `name` տիպի `string` և տպում է ողջույնի հաղորդագրություն այդ անունով:

#### Մեթոդներ վերադարձման արժեքով

Մեթոդները կարող են վերադարձնել արժեք:

```csharp
using System;

namespace MethodExamples
{
    class Program
    {
        static void Main(string[] args)
        {
            int result = Add(5, 3);
            Console.WriteLine("Արդյունքը: " + result);
        }

        static int Add(int a, int b)
        {
            return a + b;
        }
    }
}
```

Այս օրինակում `Add` մեթոդը ընդունում է երկու `int` տիպի պարամետրեր `a` և `b` և վերադարձնում է նրանց գումարը `int` տիպով:

### Գերաբեռնված մեթոդներ

C#-ում հնարավոր է ստեղծել միևնույն անունով մեթոդներ, որոնք ունեն տարբեր պարամետրերի ցուցակներ:

```csharp
using System;

namespace MethodOverloading
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine(Add(5, 3));
            Console.WriteLine(Add(5.5, 3.3));
            Console.WriteLine(Add("Բարև ", "աշխարհ"));
        }

        static int Add(int a, int b)
        {
            return a + b;
        }

        static double Add(double a, double b)
        {
            return a + b;
        }

        static string Add(string a, string b)
        {
            return a + b;
        }
    }
}
```

Այս օրինակում `Add` մեթոդը ունի երեք տարբերակ՝ ընդունելով տարբեր պարամետրեր (`int`, `double`, `string`):

### Վերադարձող բազմազանություն

Մեթոդները կարող են վերադարձնել բարդ օբյեկտներ, ինչպիսիք են զանգվածները կամ դասերը:

```csharp
using System;

namespace MethodReturnArray
{
    class Program
    {
        static void Main(string[] args)
        {
            int[] numbers = GetNumbers();
            foreach (int number in numbers)
            {
                Console.WriteLine(number);
            }
        }

        static int[] GetNumbers()
        {
            return new int[] { 1, 2, 3, 4, 5 };
        }
    }
}
```

Այս օրինակում `GetNumbers` մեթոդը վերադարձնում է `int` զանգված:

### Եզրակացություն

Մեթոդները շատ կարևոր մաս են ծրագրավորման մեջ, քանի որ դրանք թույլ են տալիս բաժանել կոդը ավելի փոքր և հարմարավետ մասերի: Հաջորդ դասերում մենք կծանոթանանք ավելի բարդ թեմաների՝ ներառելով օբյեկտ-օրիենտացված ծրագրավորում, ժառանգություն, բազմաձևություն և այլն։
